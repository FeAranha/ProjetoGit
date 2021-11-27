    Olá esse projeto mostras alguns conceitos e funcionalidades do git.

Git é  um sistema de versionamento de arquivos, auxilia o trabalho em equipe e solo. Ele trabalha com repositorios, são como pastas. Github é uma galeria de códigos, uma rede social de desenvolvedores.

- Branch é uma ramificação do projeto, são pontos no projeto, desenvolver partes e depois juntar.
- Commit é a forma de atualizar o github, postar, salvar.
- Merge é a junção da Branch segundaria, ou terceiras, com a Branch Manter(main), ele ocorre quando não há alteração na mesma linha de código. 
- Remote: https://www.atlassian.com/br/git/tutorials/syncing


Comandos


git --version: para ver a versão instalada, caso não tenha baixe do site git conforme OS.

git init: Inicializa o repositorio, e entra no tempo cronológico principal, master

git add: manda os arquivos para o stade, local de preparo do arquivo para o commit

--commit: são os pontos da nossa história, são as versões

push: empurra o commit para o repositório

pull: puxa o repositório para sua maquina 

git status: mostra informações de commit, mudanças, caso em verde quer dizer que esta no state pronto pro commit


Testes:


Criar repositorio no github com nome ProjetoGit, de modo publico sem adicionar outro readme.md, ao fazer isso é exibido comandos basicos do git, e o link do repositorio https://github.com/FeAranha/ProjetoGit.git

ps: É criado uma pasta .git na pasta do projeto, não alterar este arquivo.

git commit -m "Titulo do commit"

Ao digitar no terminal git commit -m "Primeiro commit" é realizado o commit, e se executar git status avisa que não possui commits.

Uma boa pratica é alterar o nome da branch para main:
git branch -M "main"

Após renomear para main o git exige executar o comando remote apontando para url padrão:

git remote add origin https://github.com/FeAranha/ProjetoGit.git

Nenhuma mensagem é exibida.

O comando git indica seu uso, remote faz conexão local com origin github repositorio.

Ainda não foi enviado nenhuma arquivo para o gitHub, para isso conforme indicação do github precisamos executar o comando:

git push -u origin main

Necessário login e senha do github. Ao atualizar a pagina do github podemos ver o primeiro commit.


Versionamento


Ao longo do video ocorreram alterações nos textos, e algumas correções de escrita, agora para revisar o estudo criar um novo commit:

ps: Caso executar git add . é enviado todos arquivos alterados para o state, caso queira desfazer execute git reset. Lembrando que git status mostra quais aquivos estão no state addicionandos pelo add ^^

comando clear para limpar a tela, sempre ajuda.

clear
git add Readme.md
git status

conforme status somente modifica-ra Readme.md

git commit -m "Testes e Versionamento"
git push origin main

ps: eu esqueci de salvar o vsCode logo fiz um terceiro commit.



🙏
Creditos: Rafaella Ballerini
Video Aula: https://www.youtube.com/watch?v=UBAX-13g8OM