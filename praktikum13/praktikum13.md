# Praktikum13
Selles praktikumis tegelesin skriptimisega windowsis. <br>
```
#Valmis funktsioon failist alus.ps1
#$nr:	küsimuse number
#$param: mis parameetriga tegemist (võimalikult lühidalt)
#$sisu:	väljastatav sisu
function valjasta{
	param ($nr, $param, $sisu)
	$fail = ".\tulemus.txt"
	if($sisu -eq $null){
		$rida = "$nr.${param}:	NULL"
		Write-Output $rida
		$rida | Out-File -FilePath $fail -Append
	}elseif($sisu.GetType().Name -eq "Object[]"){
		$rida = "$nr.${param}:"
		Write-Output $rida $sisu
		$rida | Out-File -FilePath $fail -Append
		$sisu | Out-File -FilePath $fail -Append
	}else{
		$rida = "$nr.${param}:	$sisu"
		Write-Output $rida
		$rida | Out-File -FilePath $fail -Append
	}
}

#Siin Väljastab kasutades funktsiooni

Valjasta 1 "Masina nimi" (hostname)
Valjasta 2 "Võrgu konfiguratsioon" (Get-WmiObject Win32_NetworkAdapterConfiguration | Select-Object -Property IPAddress, SubNetMask, DefaultIPGateway, DHCPEnabled, macaddress)
Valjasta 3 "Arvuti protsessori kirjeldus" (Get-WmiObject Win32_Processor | Select-Object -Property Caption, DeviceID, Manufacturer, MaxClockSpeed, Name, SocketDesignation)

#Siin saab füüsilise mälu ja siis teisendab selle gigabaitideks.
Valjasta 3 "Arvuti põhimälu kogus" "$([math]::Round((Get-WmiObject Win32_PhysicalMemory | Measure-Object -Property Capacity -Sum | Select-Object -Property Sum).Sum / 1GB, 2))GB"

Valjasta 4 "Graafikakaardi info" (Get-WmiObject Win32_Videocontroller | Select-Object -Property Name, DriverVersion, VideoModeDescription)
Valjasta 5 "Partitsioonitabel" (Get-Partition)
Valjasta 5 "Vaba ruum  C: kettal" "$([math]::Round((Get-Volume | Measure-Object -Property SizeRemaining -Sum | Select-Object -Property Sum).Sum / 1GB,2))GB"
Valjasta 6 "PCI siinid" (Get-WmiObject –Class Win32_PnpSignedDriver | Select-Object -Property Description, Manufacturer, DriverVersion) 
Valjasta 7 "Arvutis olevad kasutajad" (Get-LocalUser | Select-Object -Property Name, Description, LocalAccount, Enabled)
Valjasta 8 "Käimas olevad protsesside arv" ((Get-Process).count)
Valjasta 9 "Viimased 10 protsessi" $(Get-Process | Select-Object -Property Name, Id, StartTime | Sort-Object -Property StartTime | select -Last 10)
Valjasta 10 "Arvuti kuupäev ja kellaaeg" (Get-Date)
```
