    Olá esse projeto mostras alguns conceitos e funcionalidades do git, este readme.md foi feito para colocar em pratica os conceitos abordado pela Rafaella Ballerini.
    

Git é  um sistema de versionamento de arquivos, auxilia o trabalho em equipe e solo. Ele trabalha com repositorios, são como pastas. Github é uma galeria de códigos, uma rede social de desenvolvedores.

- Branch é uma ramificação do projeto, são pontos no projeto, desenvolver partes e depois juntar.
- Commit é a forma de atualizar o github, postar, salvar.
- Merge é a junção da Branch segundaria, ou terceiras, com a Branch Manter(main), ele ocorre quando não há alteração na mesma linha de código. 
- Remote: https://www.atlassian.com/br/git/tutorials/syncing


## Comandos


git --version: para ver a versão instalada, caso não tenha baixe do site git conforme OS.

git init: Inicializa o repositorio, e entra no tempo cronológico principal, master

git add: manda os arquivos para o stade, local de preparo do arquivo para o commit

--commit: são os pontos da nossa história, são as versões

push: empurra o commit para o repositório

pull: puxa o repositório para sua maquina 

git status: mostra informações de commit, mudanças, caso em verde quer dizer que esta no state pronto pro commit


## Testes:


Criar repositorio no github com nome ProjetoGit, de modo publico sem adicionar outro readme.md, ao fazer isso é exibido comandos basicos do git, e o link do repositorio https://github.com/FeAranha/ProjetoGit.git

ps: É criado uma pasta .git na pasta do projeto, não alterar este arquivo.

git commit -m "Titulo do commit"

Ao digitar no terminal git commit -m "Primeiro commit" é realizado o commit, e se executar git status avisa que não possui commits.

Uma boa pratica é alterar o nome da branch para main:

git branch -M "main"

Após renomear para main o git exige executar o comando remote apontando para url padrão:

git remote add origin https://github.com/FeAranha/ProjetoGit.git

ou

git remote set-url origin git@github.com:ppreyer/first_app.git

Nenhuma mensagem é exibida.

O comando git indica seu uso, remote faz conexão local com origin github repositorio.

Ainda não foi enviado nenhuma arquivo para o gitHub, para isso conforme indicação do github precisamos executar o comando:

git push -u origin main

Necessário login e senha do github. Ao atualizar a pagina do github podemos ver o primeiro commit.


## Versionamento


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


## Alterando e adicionando arquivos

Criar arquivo ProjetoDeFato.md contendo: Projetinho vai ser desenvolvido aqui

Refazer o processo:

git add Readme.md ProjetoDeFato.md

git status

git commit -m "Titulo do commit"

git push origin main


Caso for para todos arquivos utilizar git add .

No github ao clicar no Titulo, neste exemplo "Testes, e Versionamento", podemos ver o histórico de mudanças e adicionar comentários, porem só mostra de um commit anterior para o commit atual.


## Branch

Para uma nova função no projeto, ou alteração, feature etc, antes é necessario cria-la com o comando no exemplo Novo Botão:

git checkout -b "novo-botão"

Ao fazer isso agora tudo que for desenvolvido será realizado na Branch novo-botão. Como exemplo foi criado o arquivo new-button contendo New Button, apos alterações executar git add nomeArquivo.extencao. O push agora precisa ser em origin new-button:

git push origin new-button

Com isso atualizando a pagina github, podemos ver a main ainda sem o button e as branches, um é new-button com o arquivo criado e seu texto. Contem uma mensagem informando que esta branch esta a frente da main.

## Alteração entre Branch

É comum mudarmos de Branch e fazer alterações e voltar e mudar e ir e etc, se atentar aos commits o stash apaga alterações e afeta seu projeto fora do github, para mudar de branch execute:

git checkout main

Ou git checkout new-button para voltar.


## git merge

Para fazer a junção do desenvolvimento é utilizado o comando merge, para puxar as alterações da branch principal(main) é necessario estar nela e executar:

git checkout main //(caso esteja em outra branch)

git merge new-button

git push origin main

### Para atualizar a branch paralela com dados da principal é necessário estar sem alterações na branch paralela em questão e executar:

git branch //para listar e ver a branch selecionada

git checkout branchPrincipal // alterar para branch com atualização ou em produção para depois puxar(pull)

git pull //puxar alterações

git -b "newBranch" //cria uma nova branch

git push origin newBranch //joga as alterações na branch nova

git diff branchPrincial..newBranch //ver as diferenças entre as branchs


## git clone

Pode ser usado como uma forma de gerar backup, ou copiar o repositório de alguem. Acessar a pasta desejada e executar git clone com a url do repositório:


git clone https://github.com/rafaballerini/GitTutorial.git


lembre de favoritar os repositórios que gostou.


## git pull

Puxa as alterações no repositorio em questão.


## Fork

Copia o repositorio para seu repositorio.


## Pull Request

Ao realizar um fork de um repositório podemos desenvolver e tentar ajudar a pessoa que disponibilizou publicamente seu repositório fazendo um pull request.


🙏
- Creditos: Rafaella Ballerini
Video Aula: https://www.youtube.com/watch?v=UBAX-13g8OM

# Extra
Rank of Devs:

```
alias rank3="sort | uniq -c | sort -nr | head -n 3"
git log --format=%an | rank3
    44 fearanha
    10 maria
    10 jose
```
 Pode ser criado outros alias rank10 por exemplo e para listar os 10 mudar o -n 3 para -n 10

# Create repo terminal:

- Configurar as variáveis de ambiente GITHUB_USERNAME e GITHUB_TOKEN no arquivo .zshrc ou outro padrão e executar `source .zshrc` para carregar as variáveis de ambiente.
- Navegar até a pasta do seu projeto usando o comando cd.
- Executar `git init` para inicializar um repositório local.
- Criar o repositório no GitHub usando o comando `curl -u $GITHUB_USERNAME:$GITHUB_TOKEN https://api.github.com/user/repos -d '{"name":"<reponame>"}'`. Substitua `<reponame>` pelo nome desejado para o seu repositório.
- Ao criar copiar o 'html_url' gerado, no ex.: https://github.com/FeAranha/01-fundamentos-nodejs para usar no remmote depois
- Executar `git add .` para adicionar todos os arquivos do seu projeto ao controle de versão.
- Executar `git commit -m "start"` para fazer um commit inicial.
- Executar `git branch -M main` para renomear o branch principal para main (ou outro nome de sua preferência).
- Executar `git remote add origin <repository-url>` para adicionar o repositório remoto do GitHub. Substitua `<repository-url>` pela URL do repositório que você criou no passo 4.
- Executar `git push -u origin main` para enviar seus commits locais para o repositório remoto no GitHub.

