
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


// SCRIPT A PARTIR DA AULA 11 ATÉ A AULA 16
// GIT RESET --SOFT = DESFAZ O COMMIT E DEIXA O ARQUIVO NO STAGED PRONTO PRA COMMITA DE NOVO
// GIT RESET --MIXED = DESFAZ O COMMIT E VOLTA O ARQUIVO PRA ANTES DO STAGED (MODIFIED)
// GIT RESET --HARD = IGNORA A EXISTENCIA DO COMMIT E TUDO OQ FOI FEITO NELE

//SCRIPT

git log
commit 760d02f449c53a53a017f8b20e19ad2e252cc1ee (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:13:43 2017 -0300

  Commitando um arquivo com modificações para depois apaga-lo

commit 2c5f8f6f413086201b2b59313f12433b3ed0165f
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 20:17:58 2017 -0300

  Add arquivo Script-Git.md - Arquivo com o script dos comandos da aula até agora - Aula 10 (Visualizando o diff)

commit 9e4ce205f80e887226bc7fcde1515e37f70a5d1d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:47:27 2017 -0300

  Edit Readme.md

commit 4e3ebc801e3f9f38723725d48e95035b7b90e666
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:38:46 2017 -0300

//MODIFICAÇÃO NO ARQUIVO SCRIPT-GIT

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

      modified:   Script-Git.md

no changes added to commit (use "git add" and/or "git commit -a")

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff
diff --git a/Script-Git.md b/Script-Git.md
index 0905bbc..3d0364b 100644
--- a/Script-Git.md
+++ b/Script-Git.md
@@ -341,3 +341,9 @@ index 43ba69f..53e40bf 100644
+
+
+Goustou do curso? Quer mais? Ajude com uma doação, até um café vale!!
+
+
+// Script a partir da aula 11
+// git reset --soft = Desfaz o commit e deixa o arquivo no staged pronto pra commita de novo
+// git reset --mixed = Desfaz o commit e volta o arquivo pra antes do staged (modified)
+// git reset --hard = Ignora a existencia do commit e tudo oq foi feito nele

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git add Script-Git.md

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
(use "git reset HEAD <file>..." to unstage)

      modified:   Script-Git.md


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -m "Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset"
[master cf5c80d] Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset
1 file changed, 6 insertions(+)

// A PARTIR DAQUI COMEÇA AS MODIFICAÇÕES DA AULA

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
nothing to commit, working tree clean

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:28:12 2017 -0300

  Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset

commit 760d02f449c53a53a017f8b20e19ad2e252cc1ee
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:13:43 2017 -0300

  Commitando um arquivo com modificações para depois apaga-lo

commit 2c5f8f6f413086201b2b59313f12433b3ed0165f
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 20:17:58 2017 -0300

  Add arquivo Script-Git.md - Arquivo com o script dos comandos da aula até agora - Aula 10 (Visualizando o diff)

commit 9e4ce205f80e887226bc7fcde1515e37f70a5d1d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:47:27 2017 -0300

// MODIFIQUEI O ARQUIVO

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

      modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff // VERIFIQUEI O QUE FOI MODIFICADO
diff --git a/Readme.md b/Readme.md
index b2eefed..f03c359 100644
--- a/Readme.md
+++ b/Readme.md
@@ -1,5 +1,5 @@
# Git Course
-alskanaklsndklasdakld
+ajksannajkasnjkdn
Este é um repositorio teste para ensinar como o git funciona

Saiba mais em willianjusten.com.br

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git checkout Readme.md //APAGA A MODIFICAÇÃO QUE FOI FEITA - O ESTADO DO ARQUIVO CONTINUA MODIFIED

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff // NÃO APARECE NADA NO DIFF, POIS AS MODIFICAÇÕES FORAM APAGADAS

// MODIFIQUEI O ARQUIVO

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git add Readme.md

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
(use "git reset HEAD <file>..." to unstage)

      modified:   Readme.md


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git reset HEAD Readme.md  // RETIRA O ARQUIVO DA FILA DO STAGED - APONTA O PONTEIRO DE VOLTA PARA ONDE JÁ ESTAVA
Unstaged changes after reset:
M       Readme.md

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff
diff --git a/Readme.md b/Readme.md
index b2eefed..3a16e07 100644
--- a/Readme.md
+++ b/Readme.md
@@ -1,5 +1,5 @@
# Git Course
-alskanaklsndklasdakld
+alskanaklsndklasdakldalkdnaklanklfn
Este é um repositorio teste para ensinar como o git funciona

Saiba mais em willianjusten.com.br

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git checkout Readme.md

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
nothing to commit, working tree clean

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

      modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

// A PARTIR DAQUI SÃO OS GIT RESET - PEGA O HASH ANTERIOR AO QUE VOCÊ QUER APAGAR

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -am "Fazendo tudo de novo, pq eu resetei o terminal e perdi o script - Commitando o arquivo pra dps apagar"
[master 421f7d0] Fazendo tudo de novo, pq eu resetei o terminal e perdi o script - Commitando o arquivo pra dps apagar
1 file changed, 1 insertion(+), 1 deletion(-)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit 421f7d04c8ce7b5cf4de168c555a19010ee51aff (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:32:49 2017 -0300

  Fazendo tudo de novo, pq eu resetei o terminal e perdi o script - Commitando o arquivo pra dps apagar

commit cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2 // EM TODOS OS EXEMPLOS FOI USADO ESSE HASH
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:28:12 2017 -0300

  Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset

commit 760d02f449c53a53a017f8b20e19ad2e252cc1ee
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:13:43 2017 -0300

  Commitando um arquivo com modificações para depois apaga-lo

commit 2c5f8f6f413086201b2b59313f12433b3ed0165f
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 20:17:58 2017 -0300

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git reset --soft cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
(use "git reset HEAD <file>..." to unstage)

      modified:   Readme.md


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -m "Commitando o mesmo arquivo, apos desfazer o commit"
[master 7bfee4a] Commitando o mesmo arquivo, apos desfazer o commit
1 file changed, 1 insertion(+), 1 deletion(-)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit 7bfee4ad48e828096d451661ad536e25735f28f4 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:36:29 2017 -0300

  Commitando o mesmo arquivo, apos desfazer o commit

commit cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:28:12 2017 -0300

  Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset

commit 760d02f449c53a53a017f8b20e19ad2e252cc1ee
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:13:43 2017 -0300

  Commitando um arquivo com modificações para depois apaga-lo

commit 2c5f8f6f413086201b2b59313f12433b3ed0165f
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 20:17:58 2017 -0300


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git reset --mixed cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2
Unstaged changes after reset:
M       Readme.md

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

      modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git diff
diff --git a/Readme.md b/Readme.md
index b2eefed..132b725 100644
--- a/Readme.md
+++ b/Readme.md
@@ -1,5 +1,5 @@
# Git Course
-alskanaklsndklasdakld
+alskanaklsndklasdakldsklnasksnkska
Este é um repositorio teste para ensinar como o git funciona

Saiba mais em willianjusten.com.br

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -am "Commitando o mesmo arquivo de novo apos fazer o reset --mixed"
[master 8fad4b2] Commitando o mesmo arquivo de novo apos fazer o reset --mixed
1 file changed, 1 insertion(+), 1 deletion(-)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit 8fad4b27acc598e4074a02c2b3e919ee210330df (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:39:35 2017 -0300

  Commitando o mesmo arquivo de novo apos fazer o reset --mixed

commit cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:28:12 2017 -0300

  Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset

commit 760d02f449c53a53a017f8b20e19ad2e252cc1ee
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:13:43 2017 -0300

  Commitando um arquivo com modificações para depois apaga-lo

commit 2c5f8f6f413086201b2b59313f12433b3ed0165f
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 20:17:58 2017 -0300


Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git reset --hard cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2
HEAD is now at cf5c80d Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:28:12 2017 -0300

  Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset

commit 760d02f449c53a53a017f8b20e19ad2e252cc1ee
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:13:43 2017 -0300

  Commitando um arquivo com modificações para depois apaga-lo

commit 2c5f8f6f413086201b2b59313f12433b3ed0165f
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 20:17:58 2017 -0300

  Add arquivo Script-Git.md - Arquivo com o script dos comandos da aula até agora - Aula 10 (Visualizando o diff)

commit 9e4ce205f80e887226bc7fcde1515e37f70a5d1d
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 19:47:27 2017 -0300

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
nothing to commit, working tree clean

// A PARTIR DAQUI A AULA É SOBRE CONECTAR NUM REPOSITORIO REMOTO - É NECESSARIO CRIAR O REPOSITORIO NO GITHUB ANTES

// Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ $ git remote add origin
bash: $: command not found

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ $ git remote add origin
bash: $: command not found // COMANDO DIGITADO ERRADO

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git remote add origin https://github.com/JessPergentino/github-couser.git //CONECTA NO REPOSITORIO - O ORIGIN PODE SER QUALQUER NOME (ELE INDICA O NOME QUE SERA DADO PARA O REPOSITORIO REMOTO - A URL É DO REPOSITORIO NO GITHUB)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git remote //VERIFICA EM QUE REPOSITORIO ESTA CONECTADO
origin

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git remote -v //VERIFICA EM QUE REPOSITORIO ESTA CONECTADO DANDO MAIS DETALHES
origin  https://github.com/JessPergentino/github-couser.git (fetch)
origin  https://github.com/JessPergentino/github-couser.git (push)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git push -u origin master // AQUI ESTOU MANDANDO O QUE ESTA NO REPOSITORIO LOCAL (BRANCH MASTER) PARA O REPOSITORIO REMOTO (ORIGIN)
Counting objects: 18, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (15/15), done.
Writing objects: 100% (18/18), 4.02 KiB | 1.34 MiB/s, done.
Total 18 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), done.
To https://github.com/JessPergentino/github-couser.git
* [new branch]      master -> master
Branch master set up to track remote branch master from origin.

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.

// MODIFIQUEI O ARQUIVO PARA MANDAR PARA O REPOSITORIO REMOTO

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

      modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

// Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit - am "Fazendo mudanças no arquivo, commitando e mandando para o repositorio remoto (Github)"
error: pathspec '-' did not match any file(s) known to git.
error: pathspec 'am' did not match any file(s) known to git.
error: pathspec 'Fazendo mudanças no arquivo, commitando e mandando para o repositorio remoto (Github)' did not match any file(s) known to git. // ERRO NO COMANDO - DIGITEI ERRADO

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git commit -am "Fazendo mudanças no arquivo, commitando e mandando para o repositorio remoto (Github)"
[master 6115caf] Fazendo mudanças no arquivo, commitando e mandando para o repositorio remoto (Github)
1 file changed, 1 deletion(-)

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git log
commit 6115cafb25dd2ba5b48f9ef9fe8cc3c86f1d5bc9 (HEAD -> master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:54:27 2017 -0300

  Fazendo mudanças no arquivo, commitando e mandando para o repositorio remoto (Github)

commit cf5c80d273ca8a8e955fb3904e3fe7b8092f8ca2 (origin/master)
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:28:12 2017 -0300

  Modifiquei o arquivo Script-Git.md - Adicionei as definições dos do comando reset

commit 760d02f449c53a53a017f8b20e19ad2e252cc1ee
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Sat Nov 11 18:13:43 2017 -0300

  Commitando um arquivo com modificações para depois apaga-lo

commit 2c5f8f6f413086201b2b59313f12433b3ed0165f
Author: JessPergentino <jessicapergentino@hotmail.com>
Date:   Fri Nov 10 20:17:58 2017 -0300

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ git push origin master // MANDEI PARA O REPOSITORIO REMOTO (ORIGIN)
Counting objects: 3, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 381 bytes | 381.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/JessPergentino/github-couser.git
 cf5c80d..6115caf  master -> master

// A PARTIR DAQUI A AULA FOI SOBRE CLONE

Seventech@Seventech-PC MINGW64 ~/git-course (master)
$ cd .. // COMANDO PARA VOLTAR UM CAMINHO NO PROMPT

//Seventech@Seventech-PC MINGW64 ~
$ git clone git@github.com:JessPergentino/github-couser.git github-course-clone
Cloning into 'github-course-clone'...
The authenticity of host 'github.com (192.30.253.112)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'github.com,192.30.253.112' (RSA) to the list of known hosts.
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.// DEU ERRO E NÃO SEI PORQUE - TENTATIVA USANDO SSH

Seventech@Seventech-PC MINGW64 ~ // SAIR DA PASTA GIT-COURSE E FUI PARA A ANTERIOR
$ git clone https://github.com/JessPergentino/github-couser.git github-course-clone // URL DO REPOSITORIO QUE EU QUERO CLONAR E O NOME QUE QUERO DAR PARA ELE
Cloning into 'github-course-clone'...
remote: Counting objects: 21, done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 21 (delta 5), reused 21 (delta 5), pack-reused 0
Unpacking objects: 100% (21/21), done.

Seventech@Seventech-PC MINGW64 ~
$ ls // MOSTRA OS ARQUIVOS DENTRO DA PASTA ATUAL
'Ambiente de impressão'@
'Ambiente de rede'@
AppData/
atelier/
'Configurações locais'@
Contacts/
Cookies@
'Dados de aplicativos'@
Desktop/
Documents/
Downloads/
eclipse/
eclipse-workspace/
Favorites/
git-course/
github-course-clone/
git-jogoVelha/
hsqlprefs.dat
Intel/
Links/
'Menu Iniciar'@
'Meus documentos'@
Modelos@
Music/
NTUSER.DAT
ntuser.dat.LOG1
ntuser.dat.LOG2
NTUSER.DAT{016888bd-6c6f-11de-8d1d-001e0bcde3ec}.TM.blf
NTUSER.DAT{016888bd-6c6f-11de-8d1d-001e0bcde3ec}.TMContainer00000000000000000001.regtrans-ms
NTUSER.DAT{016888bd-6c6f-11de-8d1d-001e0bcde3ec}.TMContainer00000000000000000002.regtrans-ms
ntuser.ini
Pictures/
Recent@
'Saved Games'/
Searches/
SendTo@
Videos/
