# 1. Crearea utilizatorilor cu parolele prenumele lor
```
su
adduser trump
donald

adduser merkel 
angela

adduser putin  
vlodimir
```
# 2. Autentificare ca trump și crearea directorului și fișierului 
```
su - trump
mkdir ~/sua
echo "0123456789" > ~/sua/melania
```
# 3. Testare acces pentru alți utilizatori
# Autentificare ca putin
```
su - putin
cat /home/trump/sua/melania  # Ar trebui sa functioneze
```
# Autentificare ca merkel 
```
su - merkel
cat /home/trump/sua/melania  # Ar trebui sa functioneze
```
# 4. Afișarea permisiunilor curente
```
ls -l /home/trump/sua/melania
```

# 5. Revocarea dreptului de modificare pentru alți utilizatori
```
su - trump
chmod o-w ~/sua
```
# 6. Crearea grupului nato și adăugarea utilizatorilor
```
su
groupadd nato
usermod -aG nato merkel
usermod -aG nato trump
```
# 7. Crearea fișierului secret și modificarea permisiunilor
```
su - trump
echo "Secret info" > ~/secret
chmod 640 ~/secret    
chgrp nato ~/secret   
```

# 8. Crearea fișierului germany ca putin
```
su - putin
echo "Germany content" > ~/germany
```
# 9. Schimbarea proprietarului fișierului germany
```
su
chown merkel:merkel /home/putin/germany
```
# 10. Afișarea noului proprietar
```
ls -l /home/putin/germany
```
# 11. Modificarea parolei pentru merkel
```
passwd merkel
angelamerkel
```
# 12. Modificarea permisiunilor fișierului germany (permisiuni numerice)
```
su - merkel
chmod 600 /home/putin/germany  
```

# 13. Ștergerea contului trump cu dosarul personal
```
su
userdel -r trump
```
