## Najbitnije stvari za git

### Ime i mail
- Obicno sada ne treba, ali inace se postavlja ime i mail kad se konfigurise git
- `git config --global user.name "ovde ime ili nick"`
- `git config --global user.email "isti mail kao na git-u (GitLab, GitHub...)"`

### Pocetak
Obicno se krece tako sto se kopira neki folder sa postojeceg gita
- `git clone [url]`, url - Za gitlab koristi SSH, a za github HTTPS (kopira se sa sajta)
- `git init` za inicijalizaciju lokalnog foldera kao git repoa

### BITNO
Uvek treba proveriti u kom si branchu i koji je git status, to znaci sta se menjalo, da li je nesto dodato ili menjano
- `git branch`
- `git status`
Moze da se vidi i koje si linije menjao, to se radi sa `git diff`.
#### BITNO BITNO
Pre nego sto dodas fajlove koji ce da se komituju (`git add [file]` - za jedan ili `git add .` - za sve izmenjane), PROVERI STA SI MENJAO I STA DODAJES!!!
- `git commit -m "[poruka]"`, ovako se KOMITUJE i dok radis na lokalu, na lokalu se i komituje! MORA DA IMA PORUKA, ako nema izbacice gresku.
- `git commit -am "[poruka]"`, ovo `a` je kao add, tako da uradis i dodavanje i komit u jednoj komandi, bolje odvojeno da se radi!
Kako hoces da dodas novi branch moze `git checkout -b [ime brancha]`, a moze i `git branch [ime brancha]`. Ako hoces da se prebacis sa na neki branch `git checkout [ime brancha]`. Proveri svaki put pre rada na kom si branchu, da se ne bi zajebo.

### MNOGO BITNO
Ovde moze najvise da se zezne, ali ako se pazi nije strasno. \\
Kad si napravio lokalne komitove, onda treba to da pushujes na github, gitlab, ili nesto trece. OPET PROVERI DA LI SI DODAO SVE STO SI ZELEO, BOLJE DA DODAS MANJE NEGO VISE!!!\\
Prvi put treba da ide `git push -u origin [ime brancha]`, ovo upararuje moju lokalnu sa onom tamo. Ovo `-u` je `--set-upstream`, moze oba, samo je `-u` skraceno. Posle moze samo `git push`.\\
Kad hoces da preuzmes i spojis izmene sa nekog tamo u tvoj lokalni folder, onda `git pull`.\\
Ako hocu ekspilicitno promene sa remote maina onda `git pull origin main`. Mada bolja je opcija da se prebacis lokalno na main granu pa onda da uradis `git pull`, pa se onda vratis na svoju granu i uradis merge sa mainom.\\
