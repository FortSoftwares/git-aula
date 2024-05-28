__Danilo Almeida 27/05/2024__

# Curso Git & GitHub
- _Curso Youtube Pietro Martins De Oliveira_

## Primeiros passos
1. criação da conta no github
2. criar um repositorio   'git-aula'
3. instalar git na maquina
4. criar uma pasta local  'git-aula'
5. abrir pasta no vscode
6. Ctrl + "," pesquisar por FILE:exclude , desabilitar .git para mostrar a pasta git no vscode 
7. fazer login no github via vscode
8. criar arquivo README.md


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

