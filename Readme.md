# Github

Arquivo da aula de Git e Github para iniciantes

Comandos Básico Iniciais

1 - Defina o nome do usuário
PC@PC-IVAN MINGW64 ~/git-course
$ git config --global user.name "Ivan Carvalho"

2 - Defina o email do usuário
PC@PC-IVAN MINGW64 ~/git-course
$ git config --global user.email "ivantugal@gmail"

3 - Defina seu editor preferido (opcional - defualt = vim)
PC@PC-IVAN MINGW64 ~/git-course
$ git config --global core.editor vim

4 - Sequiser fazer inspeções, verificar as configurações do git
PC@PC-IVAN MINGW64 ~/git-course
$ git config user.name
$ git config --list (lista toda a configuração do git)

5 - Criar um diretório de trabalho
PC@PC-IVAN MINGW64 ~/git-course
$ mkdir git-course

6 - mudar para o diretório de trabalho
PC@PC-IVAN MINGW64 ~/git-course
$ cd git-course

7 - Inicializar o git para esse diretório
PC@PC-IVAN MINGW64 ~/git-course
$ git init

8 - Editar o arquibo Readme.md
PC@PC-IVAN MINGW64 ~/git-course (master)
$ vi Readme.md


Status do Ciclo de vida dos Arquivos (File status LifeCycle)

1 - Untracked (não marcado) - O arquivo acabou de ser adicionado 
no repositório mas ainda não foi visto pelo Git, ou seja, o Git
ainda não conhece em seu reposítório nenhuma versão da existência 
deste arquivo.

2 - unmodified (não modificado) - é quando o arquivo é adicionado no git,
passa a fazer parte do repositório, ele passa a ser considerado unmodified, 
ou seja ele já consta, mas não foi modificado ainda.

3 - modified (modificado) - se você editar este arquivo ele passa a o 
estado de modified, seja lá qual for a pequena modificação feita poe você. 

4 - staged (encenado, colocado em cena) - área onde vai ser criada a versão,
e estarão prontos para serem comitados, e no momento que acontecer o commit
eles voltaram ao status de unmodified.

- Verificando como está o status do git no momento
PC@PC-IVAN MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        Readme.md

nothing added to commit but untracked files present (use "git add" to track)

- Obs: O arquivo Readme.md está em untracked

- Vamos adicionar o arquivo na fila do stage
PC@PC-IVAN MINGW64 ~/git-course (master)
$ git add Readme.md

PC@PC-IVAN MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   Readme.md

- Obs: passou da fila do untracked diretamente para fila do stage, 
pronto para ser commitado.

- O que acontece se nós editarmos este arquivo novamente, antes do commit?
Para saber digite um git status:
PC@PC-IVAN MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   Readme.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   Readme.md

 - Obs: Veja que ele aparece tanto na fila do stage, como abaixo, na fila dos modifieds
 - Se eu quiser levar estas novas modificações pro commit, devo proceder conforme abaixo:
 
 PC@PC-IVAN MINGW64 ~/git-course (master)
 $ git add Readme.md
 $ git status

PC@PC-IVAN MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   Readme.md


PC@PC-IVAN MINGW64 ~/git-course (master)

- Pronto tudo certo para comitar 