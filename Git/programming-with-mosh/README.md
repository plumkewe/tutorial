# Git

Comandi affrontati sul 1/5 del [corso](https://www.youtube.com/watch?v=8JJ101D3knE) di [Programming with Mosh](https://www.youtube.com/@programmingwithmosh), che per l’ennesima volta mi ha confermato di non perdere tempo e andare direttamente a leggere la documentazione o un libro.

Cose importanti: quando usate un comando Git, scrivete -h (che sta per help) e vi uscirà una lista dei comandi disponibili. Esploratela.

## Link utili:

* [Git reference](https://git-scm.com/docs)
* [Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)

## Indice

* [Commandi](#commandi)
	* [Configurazione e Informazioni](#configurazione-e-informazioni)
		* [git --version](#git---version)
		* [git config --global user.name "Il tuo nome"](#git-config---global-username-il-tuo-nome)
		* [git config --global user.email "la-tua-email@example.com"](#git-config---global-useremail-la-tua-emailexamplecom)
		* [git config --global core.editor "code --wait"](#git-config---global-coreeditor-code---wait)
		* [git config --global -e](#git-config---global--e)
		* [git config --global core.autocrlf input](#git-config---global-coreautocrlf-input)
		* [git config --global core.autocrlf true](#git-config---global-coreautocrlf-true)
		* [git config --help e git config -h](#git-config---help-e-git-config--h)
	* [Inizializzazione e gestione del repository](#inizializzazione-e-gestione-del-repository)
		* [git init](#git-init)
		* [open .git](#open-git)
		* [rm -rf .git](#rm--rf-git)
	* [Staging Area e modifiche](#staging-area-e-modifiche)
		* [echo hello > file1.txt](#echo-hello-file1txt)
		* [git status](#git-status)
		* [git add <file-name.extention>](#git-add-file-nameextention)
		* [git add .txt](#git-add-txt)
		* [git add .](#git-add-)
		* [echo world >> file1.txt](#echo-world-file1txt)
	* [Commit](#commit)
		* [git commit -m "Messaggio del commit"](#git-commit--m-messaggio-del-commit)
		* [git commit](#git-commit)
		* [:wq](#wq)
	* [Rimozione e spostamento](#rimozione-e-spostamento)
		* [rm file2.md](#rm-file2md)
		* [git ls-files](#git-ls-files)
		* [git rm file2.txt](#git-rm-file2txt)
		* [mv file1.txt main.html](#mv-file1txt-mainhtml)
	* [File ignorati](#file-ignorati)
		* [.gitignore](#gitignore)
	* [Opzioni avanzate di rimozione](#opzioni-avanzate-di-rimozione)
		* [git rm -h](#git-rm--h)
		* [git rm --cached bin/](#git-rm---cached-bin)
		* [git rm --cached -r bin/](#git-rm---cached--r-bin)
	* [Visualizzazione delle differenze](#visualizzazione-delle-differenze)
		* [git status -s](#git-status--s)
		* [git diff --staged](#git-diff---staged)
		* [git diff](#git-diff)
		* [--global diff.tool <>](#--global-difftool-)
		* [git config --global difftool.<>.cmd "code --wait --diff $LOCAL $REMOTE"](#git-config---global-difftoolcmd-code---wait---diff-local-remote)
		* [git difftool](#git-difftool)
		* [git difftool --staged](#git-difftool---staged)
	* [Esaminare la storia](#esaminare-la-storia)
		* [git log](#git-log)
		* [git log --oneline](#git-log---oneline)
		* [git log --oneline --reverse](#git-log---oneline---reverse)
		* [git show d07ffbf](#git-show-d07ffbf)
		* [git show HEAD1](#git-show-head1)
		* [git show HEAD1:.gitignore](#git-show-head1gitignore)
		* [git ls-tree HEAD](#git-ls-tree-head)
	* [Ripristino e pulizia](#ripristino-e-pulizia)
		* [git restore --staged file.html](#git-restore---staged-filehtml)
		* [git clean](#git-clean)
		* [git clean -fd](#git-clean--fd)
		* [git restore --source=HEAD1 file.html](#git-restore---sourcehead1-filehtml)

## Commandi

### Configurazione e Informazioni

<p align="right">(<a href="#indice">indice</a>)</p>

#### `git --version`

Mostra la versione di Git installata sul tuo sistema.

* [Git Docs: --version](https://git-scm.com/docs/git-version)

#### `git config --global user.name "Il tuo nome"`

Imposta il tuo nome utente per tutti i repository locali.

* [Git Docs: config user.name](https://www.google.com/search?q=https://git-scm.com/docs/git-config%23Documentation/git-config.txt-username)

#### `git config --global user.email "la-tua-email@example.com"`

Imposta la tua email per tutti i repository locali.

* [Git Docs: config user.email](https://www.google.com/search?q=https://git-scm.com/docs/git-config%23Documentation/git-config.txt-useremail)

#### `git config --global core.editor "code --wait"`

Imposta Visual Studio Code come editor di testo predefinito per i messaggi di commit, con l'opzione `--wait` per attendere la chiusura del file.

* [Git Docs: config core.editor](https://www.google.com/search?q=https://git-scm.com/docs/git-config%23Documentation/git-config.txt-coreeditor)

#### `git config --global -e`

Apre il file di configurazione globale di Git nell'editor predefinito.

* [Git Docs: config -e](https://www.google.com/search?q=https://git-scm.com/docs/git-config%23Documentation/git-config.txt--e)

#### `git config --global core.autocrlf input`

Gestisce la conversione delle interruzioni di riga. Usato su sistemi **Linux/Mac**.

* [Git Docs: config core.autocrlf](https://www.google.com/search?q=https://git-scm.com/docs/git-config%23Documentation/git-config.txt-coreautocrlf)

#### `git config --global core.autocrlf true`

Gestisce la conversione delle interruzioni di riga. Usato su sistemi **Windows**.

* [Git Docs: config core.autocrlf](https://www.google.com/search?q=https://git-scm.com/docs/git-config%23Documentation/git-config.txt-coreautocrlf)

#### `git config --help` e `git config -h`

Mostra la documentazione completa e un riassunto delle opzioni disponibili per il comando `git config`.

* [Git Docs: config](https://git-scm.com/docs/git-config)

### Inizializzazione e gestione del repository

<p align="right">(<a href="#indice">indice</a>)</p>


#### `git init`

Inizializza un nuovo repository Git nella directory corrente.

* [Git Docs: init](https://git-scm.com/docs/git-init)

#### `open .git`

Apre la cartella `.git` (su macOS).


#### `rm -rf .git`

Cancella il repository Git.

### Staging Area e modifiche

<p align="right">(<a href="#indice">indice</a>)</p>

#### `echo hello > file1.txt`

Crea un nuovo file `file1.txt` con il contenuto "hello".

#### `git status`

Mostra lo stato del repository, inclusi i file non tracciati, le modifiche in sospeso e i file pronti per il commit.

* [Git Docs: status](https://git-scm.com/docs/git-status)

#### `git add <file-name.extention>`

Aggiunge uno o più file specifici alla **staging area**.

* [Git Docs: add](https://git-scm.com/docs/git-add)

#### `git add *.txt`

Aggiunge tutti i file con estensione `.txt` alla staging area.

* [Git Docs: add](https://git-scm.com/docs/git-add)

#### `git add .`

Aggiunge tutte le modifiche nella directory di lavoro alla staging area.

* [Git Docs: add](https://git-scm.com/docs/git-add)

#### `echo world >> file1.txt`

Aggiunge il testo "world" alla fine del file `file1.txt`.

### Commit

<p align="right">(<a href="#indice">indice</a>)</p>

#### `git commit -m "Messaggio del commit"`

Crea un nuovo commit con il messaggio fornito.

* [Git Docs: commit](https://git-scm.com/docs/git-commit)

#### `git commit`

Apre l'editor di testo predefinito per scrivere un messaggio di commit più dettagliato.

* [Git Docs: commit](https://git-scm.com/docs/git-commit)

#### `:wq`

Salva ed esce dall'editor **Vim**.

### Rimozione e spostamento

<p align="right">(<a href="#indice">indice</a>)</p>

#### `rm file2.md`

Cancella il file `file2.md` dal sistema operativo.

#### `git ls-files`

Mostra un elenco dei file tracciati da Git.

* [Git Docs: ls-files](https://git-scm.com/docs/git-ls-files)

#### `git rm file2.txt`

Rimuove il file dalla staging area e lo cancella dal sistema operativo.

* [Git Docs: rm](https://git-scm.com/docs/git-rm)

#### `mv file1.txt main.html`

Rinomina il file `file1.txt` in `main.html`.

### File ignorati

<p align="right">(<a href="#indice">indice</a>)</p>

#### `.gitignore`

Un file di testo che elenca i file e le directory che Git deve ignorare.

* [Git Docs: gitignore](https://git-scm.com/docs/gitignore)

### Opzioni avanzate di rimozione

<p align="right">(<a href="#indice">indice</a>)</p>

#### `git rm -h`

Mostra la documentazione e le opzioni disponibili per il comando `git rm`.

* [Git Docs: rm](https://git-scm.com/docs/git-rm)

#### `git rm --cached bin/`

Rimuove la directory `bin` dalla staging area, ma la mantiene nel file system.

* [Git Docs: rm --cached](https://www.google.com/search?q=https://git-scm.com/docs/git-rm%23Documentation/git-rm.txt---cached)

#### `git rm --cached -r bin/`

Rimuove la directory `bin` dalla staging area e tutti i suoi contenuti, ma li mantiene nel file system. L'opzione `-r` sta per "ricorsivo".

* [Git Docs: rm --cached](https://www.google.com/search?q=https://git-scm.com/docs/git-rm%23Documentation/git-rm.txt---cached)

### Visualizzazione delle differenze

<p align="right">(<a href="#indice">indice</a>)</p>

#### `git status -s`

Mostra una versione abbreviata e più concisa dello stato del repository.

* [Git Docs: status -s](https://www.google.com/search?q=https://git-scm.com/docs/git-status%23Documentation/git-status.txt--s)

#### `git diff --staged`

Mostra le differenze tra la staging area e l'ultimo commit.

* [Git Docs: diff --staged](https://www.google.com/search?q=https://git-scm.com/docs/git-diff%23Documentation/git-diff.txt---staged)

#### `git diff`

Mostra le differenze tra la directory di lavoro e la staging area.

* [Git Docs: diff](https://git-scm.com/docs/git-diff)

#### `--global diff.tool <>`

Questa non è una linea di comando completa, ma una parte della configurazione. Serve per impostare uno strumento di visualizzazione delle differenze esterno.

* [Git Docs: diff.tool](https://www.google.com/search?q=https://git-scm.com/docs/git-config%23Documentation/git-config.txt-difftool)

#### `git config --global difftool.<>.cmd "code --wait --diff $LOCAL $REMOTE"`

Configura Visual Studio Code come strumento per visualizzare le differenze.

* [Git Docs: git-difftool](https://git-scm.com/docs/git-difftool)

#### `git difftool`

Avvia lo strumento di visualizzazione delle differenze configurato.

* [Git Docs: git-difftool](https://git-scm.com/docs/git-difftool)

#### `git difftool --staged`

Avvia lo strumento di visualizzazione delle differenze per le modifiche nella staging area.

* [Git Docs: git-difftool](https://git-scm.com/docs/git-difftool)

### Esaminare la storia

<p align="right">(<a href="#indice">indice</a>)</p>

#### `git log`

Mostra la storia completa dei commit.

* [Git Docs: log](https://git-scm.com/docs/git-log)

#### `git log --oneline`

Mostra una versione più compatta della storia dei commit.

* [Git Docs: log --oneline](https://www.google.com/search?q=https://git-scm.com/docs/git-log%23Documentation/git-log.txt---oneline)

#### `git log --oneline --reverse`

Mostra la storia dei commit su una riga, dal più vecchio al più recente.

* [Git Docs: log --reverse](https://www.google.com/search?q=https://git-scm.com/docs/git-log%23Documentation/git-log.txt---reverse)

#### `git show d07ffbf`

Mostra i dettagli di un commit specifico usando il suo hash.

* [Git Docs: show](https://git-scm.com/docs/git-show)

#### `git show HEAD~1`

Mostra i dettagli del commit precedente all'ultimo (HEAD).

* [Git Docs: show](https://git-scm.com/docs/git-show)

#### `git show HEAD~1:.gitignore`

Mostra il contenuto del file `.gitignore` come era nel commit precedente all'ultimo.

* [Git Docs: show](https://git-scm.com/docs/git-show)

#### `git ls-tree HEAD`

Elenca il contenuto di un albero di commit (tipicamente l'ultimo).

* [Git Docs: ls-tree](https://git-scm.com/docs/git-ls-tree)

### Ripristino e pulizia

<p align="right">(<a href="#indice">indice</a>)</p>

#### `git restore --staged file.html`

Rimuove un file dalla staging area.

* [Git Docs: restore --staged](https://www.google.com/search?q=https://git-scm.com/docs/git-restore%23Documentation/git-restore.txt---staged)

#### `git clean`

Rimuove i file non tracciati dalla directory di lavoro.

* [Git Docs: clean](https://git-scm.com/docs/git-clean)

#### `git clean -fd`

Rimuove i file e le directory non tracciate.

* [Git Docs: clean](https://git-scm.com/docs/git-clean)

#### `git restore --source=HEAD~1 file.html`

Ripristina un file allo stato in cui si trovava nel commit precedente all'ultimo.

* [Git Docs: restore](https://git-scm.com/docs/git-restore)