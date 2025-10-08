# Comenzi pentru exercitiul dat

Presupunem că numele este Popescu și prenumele Ion.

1. Creare director cu numele datei de mâine și deschiderea lui, apoi crearea altor 3 directoare:

```bash
maine=$(date -d "tomorrow" +%Y-%m-%d)
mkdir "$maine"
cd "$maine"
mkdir Popescu
mkdir Ion
mkdir Popescu_Ion
```
2. Crearea fișierelor 1nu și 2oi, și scrierea textului în fișierul 1nu, apoi redenumirea lui în Lumina:
```
touch 1nu 2oi
cat > 1nu << EOF
Lumina ce-o simt
năvălindu-mi în piept când te văd,
oare nu e un strop din lumina
creată în ziua dintâi,
din lumina aceea-nsetată adânc de viaţă?
Nimicul zăcea-n agonie
când singur plutea-ntuneric şi dat-a
un semn Nepătrunsul:
"Să fie lumină!".
EOF
mv 1nu Lumina
``` 

3. Copierea fișierului Lumina în directorul Popescu și mutarea fișierului 2oi în directorul Ion cu redenumirea în Lumina2:
```
cp Lumina Popescu/
mv 2oi Ion/Lumina2
```

4. Copierea directorului Popescu în directorul Popescu_Ion:

```
cp -r Popescu Popescu_Ion/
```

5. Afișarea conținutului directorului rădăcină (cu fișiere ascunse) și afișarea conținutului fișierului Lumina:

```
cd ..
ls -la
cat "$maine/Lumina"
```

6. Afișarea ultimei linii din fișierul Lumina:

```
tail -n 1 "$maine/Lumina"
```

7. Afișarea cuvântului "agonie" și a numărului liniei în care se află:
```
grep -n "agonie" "$maine/Lumina"
```

8. Înlocuirea cuvântului "lumină" cu "ziuă" în fișierul Lumina:
```
sed -i 's/lumină/ziuă/g' "$maine/Lumina"
```

9. Ștergerea directorului Popescu_Ion:
```
rm -r "$maine/Popescu_Ion"
```

10. Afișarea calendarului pentru august 1944 și setarea opririi sistemului peste 30 de minute:

```
cal 8 1944
sudo shutdown -h +30
```





















