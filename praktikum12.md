# Praktikum12
Selles praktikumis tegelesin linux skriptimisega. <br>

#### Ülesanne 3 <br>
```
#!/bin/bash

echo "Sisesta oma nimi:" 
read nimi
echo "Sisesta oma eriala:"
read eriala
echo "Sisesta oma matriklinumber:"
read matriklinumber

echo "Nimi: $nimi"
echo "Eriala: $eriala"
echo "Matrikli number: $matriklinumber"
```
![image](https://github.com/user-attachments/assets/1aa2d31a-56e5-4243-85c5-abaab60fd62f)

#### Ülesanne 4 <br>
```
#!/bin/bash

laiend_a=$1
laiend_b=$2

for fail in $(ls)
do
    if [ ${fail##*.} = $laiend_a ] 
    then
        mv $fail ${fail%.*}.$laiend_b
    fi
done
```
![image](https://github.com/user-attachments/assets/bf0bfa34-26da-45c5-8b0d-605056c12223)

#### Ülesanne 5 <br>
```
#!/bin/bash

IFS=$'\n'

protsess=$1

for line in $(ps -A)
do
    if [[ $(echo "$line" | tr -s ' ' | cut -d ' ' f5) == "$protsess" ]]
    then
        echo $line | tr -s ' ' | cut -d ' ' -f5
        echo $line | tr -s ' ' | cut -d ' ' -f2
    fi
done
```
![image](https://github.com/user-attachments/assets/e6a724df-1f39-422d-abd0-a52207599a75)

#### Ülesanne 6 <br>
```
#!/bin/bash

astenda() {
    a=$1
    b=$2
    vastus=1

    while [ $b -gt 0 ]
    do
        vastus=$(($vastus * $a))
        b=$(($b - 1))
    done
    echo $vastus
}

echo $(astenda 9 5)
```
![image](https://github.com/user-attachments/assets/3bb09570-76f7-4ae9-a6e6-b9105bb17259)

#### Ülesanne 7 <br>
Minu küsimus <br>
![image](https://github.com/user-attachments/assets/51117fea-6375-4843-a525-6180dffa0571)
AI vastus <br>
![image](https://github.com/user-attachments/assets/0bdd83be-81ad-4d82-b657-213627008cb0)
![image](https://github.com/user-attachments/assets/3ed71088-1cd4-4c23-ace2-d1e4374353ca)



