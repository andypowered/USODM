# Comenzile : 

- Cei care nu au, descarca Git bash si instaleaza https://git-scm.com/downloads, si configureaza numele de utilizator si adresa de email.
```
git config --global user.name "Andy_Powered"
git config --global user.email "andreigultur@gmail.com"

```
- Afisati lista setarilor instalate.
```
git config --list
```
- Pozitionati-va pe desktop
```
cd ~/Desktop
```
- Creati un folder pe desktop cu denumirea Numele, prenumele si grupa dvs. (ex. Carp Alex P-1641)
```
mkdir andrei gultur w-222
```
- Creati un folder cu denumirea To Delete și imediat dupa asta stergeti directoriul dat (prin comanda).
```
mkdir "To Delete" | rmdir -f "To Delete"
```
- Initiati un repozitoriu in folderul cu numele dvs.
```
cd "andrei gultur w-222" | git init
```
- Creati 4 fisiere prin comanda corespunzatoare : 1.txt, 2.docx, 3.txt, 4.txt.
```
touch {1,3,4}.txt 2.docx
```
- Rulati git status.
```
git status
```
 
# Screenshots :

![screenshot](https://github.com/andypowered/USODM/blob/main/git/1.png)

![screenshot](https://github.com/andypowered/USODM/blob/main/git/2.png)

![screenshot](https://github.com/andypowered/USODM/blob/main/git/3.png)

![screenshot](https://github.com/andypowered/USODM/blob/main/git/4.png)

![screenshot](https://github.com/andypowered/USODM/blob/main/git/5.png)
