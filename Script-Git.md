
Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git init // INICIALIZOU UM NOVO REPOSITORIO
Reinitialized existing Git repository in C:/Users/Seventech/git-course/.git/

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status //VERIFICOU O STATUS DO REPOSITORIO
On branch master // Aqui o Git informa em que branch vc está - Neste caso master

No commits yet // NÃO HOUVE COMMITS

nothing to commit (create/copy files and use "git add" to track) // SEM ARQUIVOS PARA COMMITAR

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ ls // MOSTRA A LISTA DE ARQUIVOS NA PASTA

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

// Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ subl
bash: subl: command not found

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ subl Readme.md
bash: subl: command not found

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ sublime Readme.md
bash: sublime: command not found // - TENTEI ABRIR O SUBLIME PELO TERMINAL E NÃO DEU CERTO

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git config core.editor "C:\Program Files\Sublime Text 3\sublime_text.exe" // SETTA O EDITOR QUE SERÁ UTILIZADO - NESTE CASO O SUBLIME

// Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ sublime Readme.md
bash: sublime: command not found // TENTEI CRIAR NOVAMENTE O ARQUIVO PELO TERMINAL

// CRIEI O ARQUIVO DIRETAMENTE PELO ATOM - ADICIONEI A PASTA DO REPOSITORIO COMO UM NOVO PROJETO E CRIEI UM NOVO ARQUIVO.

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status // VERIFIQUEI O REPOSITORIO
On branch master

No commits yet

Untracked files: // O GIT ACHOU UM ARQUIVO QUE AINDA NÃO FOI VERSIONADO - UNTRACKED
  (use "git add <file>..." to include in what will be committed)

        Readme.md

nothing added to commit but untracked files present (use "git add" to track)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git add Readme.md // AQUI EU ADICIONO O ARQUIVO PARA QUE ELE POSSA SER VERCIONADO PELO GIT - ELE PASSA A SER UNMODIFIED

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status // AQUI O GIT INFORMA QUE TEM UM ARQUIVO PRONTO PARA SER COMMITADO
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   Readme.md


// AQUI EU MODIFICO O ARQUIVO

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status //VERIFICO O STATUS DE NOVO
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   Readme.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   Readme.md // O GIT AVISA QUE O ARQUIVO FOI MODIFICADO, NECESSITANDO QUE SEJA ADICIONADO - MODIFIED


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git add Readm.md
fatal: pathspec 'Readm.md' did not match any files

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git add Readme.md // ADICIONO O ARQUIVO - STAGED

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status // VERIFICO E O GIT INFORMA QUE O ARQUIVO ESTÁ PRONTO PARA SER COMMITADO - STAGED
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   Readme.md


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -m "Add Readme.md - primeiro commit de teste"  // FAÇO O PRIMEIRO COMMIT DO ARQUIVO
[master (root-commit) 34cbd92] Add Readme.md - primeiro commit de teste
 1 file changed, 3 insertions(+)
 create mode 100644 Readme.md

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status //VERIFICO O STATUS E O ARQUIVO VOLTA A SER UNMODIFIED
On branch master
nothing to commit, working tree clean

//MODIFICO O ARQUIVO NOVAMENTE

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -m "vai dar erro"
On branch master
Changes not staged for commit:
        modified:   Readme.md

no changes added to commit

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git add Readme.md

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   Readme.md


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -m "Add saiba mais"
[master 4e3ebc8] Add saiba mais
 1 file changed, 2 insertions(+)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log // MOSTRA O HISTORICO DE COMMITS - AQUI TBM É POSSIVEL VER O HASHCODE DOS COMMITS
commit 4e3ebc801e3f9f38723725d48e95035b7b90e666 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:38:46 2017 -0300

    Add saiba mais

commit 34cbd92c49ba956bed0b1b32036c990e45d8815d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:34:53 2017 -0300

    Add Readme.md - primeiro commit de teste

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log --decorate
commit 4e3ebc801e3f9f38723725d48e95035b7b90e666 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:38:46 2017 -0300

    Add saiba mais

commit 34cbd92c49ba956bed0b1b32036c990e45d8815d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:34:53 2017 -0300

    Add Readme.md - primeiro commit de teste

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log --author="Jess" //MOSTRA OS COMMITS POR AUTOR
commit 4e3ebc801e3f9f38723725d48e95035b7b90e666 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:38:46 2017 -0300

    Add saiba mais

commit 34cbd92c49ba956bed0b1b32036c990e45d8815d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:34:53 2017 -0300

    Add Readme.md - primeiro commit de teste

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git shortlog // UMA FORMA MAIS SIMPLIFICADA DE MOSTRAR OS COMMITS
JessPergentino (2):
      Add Readme.md - primeiro commit de teste
      Add saiba mais


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git shortlog -sn // AQUI MOSTRA APENAS O NUMERO DE COMMITS FEITO POR CADA AUTOR
     2  JessPergentino

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log --graph // MOSTRA EM FORMA DE GRAFICO O HISTORICO DE COMMITS
* commit 4e3ebc801e3f9f38723725d48e95035b7b90e666 (HEAD -> master)
| Author: JessPergentino <jessicapergentino@hotmail.com>
| Date:   Fri Nov 10 19:38:46 2017 -0300
|
|     Add saiba mais
|
* commit 34cbd92c49ba956bed0b1b32036c990e45d8815d
  Author: JessPergentino <jessicapergentino@hotmail.com>
  Date:   Fri Nov 10 19:34:53 2017 -0300

      Add Readme.md - primeiro commit de teste

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit 4e3ebc801e3f9f38723725d48e95035b7b90e666 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:38:46 2017 -0300

    Add saiba mais

commit 34cbd92c49ba956bed0b1b32036c990e45d8815d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:34:53 2017 -0300

    Add Readme.md - primeiro commit de teste

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git show 4e3ebc801e3f9f38723725d48e95035b7b90e666
commit 4e3ebc801e3f9f38723725d48e95035b7b90e666 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:38:46 2017 -0300

    Add saiba mais

diff --git a/Readme.md b/Readme.md
index 955cec7..43ba69f 100644
--- a/Readme.md
+++ b/Readme.md
@@ -1,3 +1,5 @@
 # Git Course

 Este é um repositorio teste para ensinar como o git funciona
+
+Saiba mais em willianjusten.com.br

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
nothing to commit, working tree clean

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff //MOSTRA AS MODEFICAÇÕES FEITAS NO ARQUIVO - BOA PRATICA: SEMPRE FAZER UM DIFF ANTES DO COMMIT
diff --git a/Readme.md b/Readme.md
index 43ba69f..53e40bf 100644
--- a/Readme.md
+++ b/Readme.md
@@ -3,3 +3,6 @@
 Este é um repositorio teste para ensinar como o git funciona

 Saiba mais em willianjusten.com.br
+
+
+Goustou do curso? Quer mais? Ajude com uma doação, até um café vale!!

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff --name-only //MOSTRA APENAS O NOME DO ARQUIVO MODIFICADO
Readme.md

// Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ g s
bash: g: command not found // COMANDO INEXISTENTE

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -am "Edit Readme.md" // FAZ O ADD E O COMMIT JUNTOS
[master 9e4ce20] Edit Readme.md
 1 file changed, 3 insertions(+)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit 9e4ce205f80e887226bc7fcde1515e37f70a5d1d (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:47:27 2017 -0300

    Edit Readme.md

commit 4e3ebc801e3f9f38723725d48e95035b7b90e666
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:38:46 2017 -0300

    Add saiba mais

commit 34cbd92c49ba956bed0b1b32036c990e45d8815d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:34:53 2017 -0300

    Add Readme.md - primeiro commit de teste

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git show 9e4ce205f80e887226bc7fcde1515e37f70a5d1d
commit 9e4ce205f80e887226bc7fcde1515e37f70a5d1d (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:47:27 2017 -0300

    Edit Readme.md

diff --git a/Readme.md b/Readme.md
index 43ba69f..53e40bf 100644
--- a/Readme.md
+++ b/Readme.md
@@ -3,3 +3,6 @@
 Este é um repositorio teste para ensinar como o git funciona

 Saiba mais em willianjusten.com.br
+
+
+Goustou do curso? Quer mais? Ajude com uma doação, até um café vale!!
