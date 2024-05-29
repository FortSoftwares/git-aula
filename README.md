__Danilo Almeida 27/05/2024__
_Curso Youtube Pietro Martins De Oliveira_

### Primeiros passos
1. criação da conta no github
2. criar um repositorio   'git-aula'
3. instalar git na maquina
4. criar uma pasta local  'git-aula'
5. abrir pasta no vscode
6. Ctrl + "," pesquisar por FILE:exclude , desabilitar .git para mostrar a pasta git no vscode 
7. fazer login no github via vscode
8. criar arquivo README.md

### Login no github
git config --global user.name "Seu Nome"

git config --global user.email "seuemail@example.com"


### Inicializa git na pasta local
git init

### Adiciona unico arquivo para commit
git add README.md

### Adicionar todos arquivos para commit
git add .

### Verifica status do processo
git status

### Faz o commit para pasta local incluindo a msg do commit
git commit -m "Mensagem do comit"

### Verifica o Log do que foi feito
git log

### Ou verifica Log de commit mostrando apenas a linha principal
git log --pretty=oneline

### Mostrar as alterações feitas antes de add e executar o commit
git diff

### Retirando determinado arquivo do processo de add .
git restore --staged README.md

### Renomeando a branch
_Renomeando a branch master criada automaticamente pelo git para branch main, pra ficar em conformidade com o github_
git branch -M main

### Verificar em qual branch estamos
git branch

### Conectando repositório local com o GitHub
_Ao criar um repositório no github e acessar ele, aparece esse comando um pouco abaixo nos códigos._
git remote add origin https://github.com/FortSoftwares/git-aula.git

### Verificar em qual repositório remoto estamos conectados
git remote get-url origin

### Fazer o primeiro envio de arquivos para o repositório do GitHub
git push -u origin main

_Executar um git log para ver detalhes do primeiro push_
_Nesse momento já teremos os arquivos do projeto no github_

### Enviar commit para o github
_uitilizado após git add . e git commit -m "msg"_
_Após o primeiro push eu não preciso excutar mais __git push -u origin main__ posso executar apenas_

git push

### Comitando diretamente sem precisar executar _git add ._ antes
git commit -am "msg"


### Extenções para o vscode
1. Git History
_Clicar com botão direito na area vazia do painel de arquivos do vscode e selecionar Git View Fille History_

2. Git Graph


### Mostrar as ultimas atualizações e quem fez elas em um arquivo
git blame README.md


# Trablhando com Branchs

### Criando nova branch
- criar
git checkout -b "nova-feature"
- verificar
git log --pretty=oneline
- verificar em qual branch estou _o asterisco mostra em qual estou atuamente_
git branch

### Push da nova branch
git push -u origin nova-feature


### Mudar de branch
_Nesse exemplo mudo para branch main_
git checkout main
_Conferindo a branch atual_
git branch

### puxar os arquivos da branch atual remota para o local
git pull


### Mesclando com Merge
_supondo que eu esteja no main, executando esse comando eu meslclo a branch novo-fix com a man, localmente_
git merge "novo-fix" 

### Apagando Branch local
_no caso aqui deleto a branch nova-feature, localmente_
git branch -d nova-feature

### Apagando Branch remoto
_no caso aqui deleto a branch nova-feature, que esta no github_
push -d origin novo-fix

### Git Stash 
_Guardando código para uma futura continuação_


### Revertendo um commit
_aqui reverto o ultimo commit no caso oque esta no HEAD_
git revert HEAD --no-edit

_aqui reverto o commit definido pelo hash do commit_
git revert HASH --no-edit

_concluir com git push para atualizar o repositorio do github_

### Reset
_Resetando a configuração de um commit_
git reset HEAD --hard

### Reset commit (perigoso, reseto tudo depois do hash definido)
git reset 35f811dcdb5433ebd009bcdc3d75229b7cba3e1f --hard




# Fluxograma de Desenvolvimento e Versionamento

### Linha do tempo criada pelo GPT

- Início do Desenvolvimento: Criação do Repositório no GitHub
- Configuração Inicial: Clone do Repositório e Configuração do Git
- Desenvolvimento Continuado: Criação de Branch develop, Branch de Funcionalidade, Desenvolvimento, Integração na Develop
- Preparação para Release: Criação de Branch de Release, Teste e Ajustes
- Entrega Final: Merge na Main, Criação de Tag, Push Tags



## Início do Desenvolvimento:

### Ação: Criação do Repositório no GitHub
- Detalhe: Vá para GitHub, crie um novo repositório.
- Clone do Repositório:

### Ação: Clonar o Repositório
- Comando: git clone URL
- Configuração do Git:

### Ação: Configurar o Git
- Comando: git config --global user.name "Seu Nome"
- Comando: git config --global user.email "seuemail@example.com"
- Criação de Branch develop:

### Ação: Criar a branch develop
- Comando: git checkout -b develop main
- Branch de Funcionalidade:

### Ação: Criar uma branch de funcionalidade
- Comando: git checkout -b feature/nome-da-funcionalidade develop
- Desenvolvimento:

### Ação: Desenvolver a funcionalidade
- Comando: git add .
- Comando: git commit -m "Descrição do que foi feito"
- Comando: git push origin feature/nome-da-funcionalidade
- Integração na Develop:

### Ação: Integrar a funcionalidade na develop
- Comando: git checkout develop
- Comando: git pull origin develop
- Comando: git merge feature/nome-da-funcionalidade
- Comando: git push origin develop
- Branch de Release:

### Ação: Criar a branch de release
- Comando: git checkout -b release/vX.X.X develop
- Teste e Ajustes:

### Ação: Testar e ajustar a release
- Detalhe: Correção de Bugs e Ajustes finais
- Merge na Main:

### Ação: Fazer merge na main
- Comando: git checkout main
- Comando: git pull origin main
- Comando: git merge release/vX.X.X
- Comando: git push origin main
- Criação de Tag:

### Ação: Criar uma tag para a versão
- Comando: git tag -a vX.X.X -m "Release versão X.X.X"
- Push Tags:

### Ação: Enviar tags para o repositório remoto
- Comando: git push origin main --tags

