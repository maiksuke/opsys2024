# Praktikum9
Käesolevas praktikumis lahendasin ülesandeid windowsis ja linuxis. Õppisin protsesside uurimist. <br>


|Küsimus|Linux|Windows|Linuxis kasutatud käsklus|Windowsis kasutatud tööriist|
|---|---|---|---|---|
|Mitu protsessi kokku arvutis käib?|215|121|ps -aux | wc -l|Task manager|
|Milline on kõige esimesena käivitatud protsess?|/sbin/init splash|System|ps axo pid,cmd,comm,etime|Task manager|
|Milliste kasutajate protsesse arvutis käib?|mairon, root, system+|Mairon|ps aux|Task manager|
|Kui kaua on arvuti järjest töötanud?|17 min|12 minutit|uptime|Task manager|
|Milline protsess käivitati kõige hiljem?|tail|Service Control Manager|ps -eo comm,lstart,cmd --sort=start_time | tail -n 1|Task manager|
|Milline on kõige rohkem protsessoriaega võttev protsess ja kui mitu protsenti protsessoriajast ta tarbib?|gnome-shell 56.25%|Taskmgr 13%|System monitor|Task manager|
|Milline on kõige rohkem virtuaalmälu võttev protsess?|lubuntu-upg-notifier.sh|Windowsi vidinad|System monitor|Task manager|
|Milline on kõige rohkem füüsilist mälu võttev protsess?|gnome-shell|wsappx|System monitor|Task manager|
|Kui palju füüsilisest mälust on vaba ja kui palju hõivatud?|Kasutusel 1.2 GB, saadaval 1.9 GB|Kasutusel 2.7 GB, saadaval 1.3 GB|System monitor|Task manager|
|Kui palju on põhikettal vaba ruumi mahult (GB) ja protsentuaalselt?|11.3 GB 47%|27.6|System monitor|File explorer|
|Milline on kõige suurem arvutis olev fail ja kõige rohkem andmemahtu hõivav kaust?|   |Windows kaust. msedge.dll|   |WinDirStat|
|millisele CPU alamtegevusele kulub enim protsessori aega kummagi käsu puhul?|Esimene kasutab 99%. Teine kasutab 95%.||top||
|Milline protsess kõige rohkem salvestusseadmele kirjutab?|   |System|   |Resource Monitor|
|Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab?|   |swapfile.sys|   |Resource Monitor|
|Milline protsess kõige rohkem salvestusseadmelt loeb?|   |WmiPrvSE.exe|   |Resource Monitor|
|Millisest failist eelmise küsimuse protsess kõige rohkem loeb?|   |WmiPerfClass.dll|   |Resource Monitor|
|Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? |   |2001:bb8:2003:f:898b:881d:c240:6936, 61487, 2a00:1450:4026:808::200a, 443, 11, 6019 B|   |Resource Monitor|
|Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud.|   |Lasen Avada task manageri ja vaatan cpu, gpu, ram kasutust, et kas miskit kasutab liiga palju.|   |Task manager|
<br>


#### 12. <br>
![Screenshot 2024-11-06 021633](https://github.com/user-attachments/assets/aa547c0d-b219-4e1e-973c-68af7a5e95c1)
 <br>
#### 14. <br>
![Screenshot 2024-11-05 235130](https://github.com/user-attachments/assets/45a4cfc8-282c-45e0-9b48-a2ee30d177f1)
