## Comandos git

### Há duas maneiras de trabalhar com git
- caso já tenha uma repo local <br>
criar um repo remoto pelo github (nota não adicionar readme e nem gitignore para não da conflitos) e depois fazer um push <br>
- caso queira trabalhar em um projeto do zero <br>
criar um repo remoto pelo github adiciona readme e gitignore e fazer um pull do repo remoto <br> <br> <br> <br>

#### Alguns conceitos chaves no git
- blob: objeto associado aos arquivos (contém uma chave sha1 associado ao objeto)
- tree: equivalente a diretório, uma tree contém metadados e blobs, e também outras trees (também contém uma chave sha1 associada a tree)
- commit: engloba os blobs, trees e outros metadados (contém chave sha1 associado ao commit)
- nota: qualquer alteração numa blob se refletirá nas trees, assim sendo mudando sua chave sha1 associada. <br><br><br><br>

#### gerando uma chave ssh para poder te acesso livre ao seu github
- 1- gerar chave ssh: ssh-keygen -t ed25519 -c nome@email.com (vai gerar dois arquivos, um publico e outro privado)
- 2- adiciona o conteudo da chave publica ao seu github (se localiza nas configurações do seu github)
- 3- iniciar o agente ssh:  eval $(ssh-agent -s)
- 4- adicionar a chave ao agente ssh: ssh-add [chave privada] <br><br><br><br>


- git config --global user.name "Alan Cavalcante" - configura o nome <br>
- git config --global user.email "user@domain.com" - configura email <br>
- git config --global user.editor vscode - configura o editor de texto <br>
- git config --global user.user "Alan589" - configura o nome de usuario<br>
- git config --global --unset user.name/user.email/etc <br><br><br><br>


- git config user.name - mostra o usuário cadastrado <br>

- git config user.email - mostra email cadastrado <br>
- git config --list - mostra todos dados cadastrados <br><br><br><br>

- git init - cria e inicializa um repositório (dê o comando dentro da pasta)<br>
- git status - informa o "status" atual do repositório (todas as modificações feitas na pasta) <br><br><br><br>

- git add (file) ou git add -A - adiciona arquivo ao projeto (untracked/modified para tracked) <br>
(-A: todos os arquivos ou (file): manualmente) <br> 
- git add . - adiciona todos os arquivos tanto untracked e modified <br><br><br><br>

- git commit -m "msg" / git -m "msg" -m "descrição" - cria um versionamento do projeto <br>
- git clone (ssh) <br>
- git merge (nome da branch) <br>
- git remote add [nome da repo remoto] ssh - adiciona um repositório remoto ao repositório local <br>
nota: [nome da repo remoto] - nomeia o repo remoto 
- git push -u [nome do repo remoto] [nome da branch] - envia o repositório local para o remoto (-u grava push padrão) <br>
[nome da branch remota] é o nome que você deu ao nomear o repo pelo git remote add, [nome da branch]  é a branch que você quer enviar os arquivos ex: se quiser enviar pra branch principal da repo remota coloque 'main' ou coloque o nome da branch que quiser 
- git remote / git remote -v - lista o repositorio remoto
- git pull https - 'puxa' o repo remoto para o local 
- git pull [remote repo] [local repo branch] - puxa a repo remoto para atualizar com a repo local
- git push [nome do repo remoto] --delete [nome da branch que quer deletar]


- git log - lista todos os commits feitos no branch atual <br>
- git branch - lista todas as branches do projeto <br><br><br><br><br>

- git commit -am "msg" - add o arquivo e da commit em seguida (funciona somente se o arquivo estiver em modified ou pronto para da commit) <br><br><br>

- git reset --soft (hash) - desfaz um commit para um ponto anterior (hash) e mantém o arquivo pronto para da commit novamente (diferente do mixed, o soft ele mantém o git add file<br>
- git reset --mixed (hash) - desfaz um commit para um ponto anterior (hash) e mantém o arquivo em modified (volta ao um ponto anterior, porém as modificações sao mantidas no arquivo)<br>
- git reset --hard (hash) - desfaz um commit para um ponto anterior (hash) e deleta todos os arquivos criados e modificados (volta ao um ponto anterior, porém as modificações sao desfeitas do arquivo) <br><br><br><br>

- git reset (hash) - desfaz commit porém mantém as alterações atual <br>
- git reset HEAD~x - desfaz commit (x é quantos commit você quer voltar) <br>
- git reset (nome do arquivo) / git reset - unstage um arquivo ou todos os arquivos <br>
- git checkout HEAD -- (nome do arquivo) - desfaz as modificações feitas no arquivo <br><br><br><br><br>

- git branch (nome da branch) - cria uma nova branch a parti da branch atual <br>
- git branch -d (nome da branch) - deleta uma branch <br>
- git checkout (nome da branch) - muda de branch <br>
- git checkout -b (nome da branch) - cria e muda para uma nova branch <br><br><br><br>

- git diff / git diff (nome do arquivo) / git diff --name-only - mostra as modificações feitas nos arquivos do projeto <br><br><br><br>


- git log --decorate / git log --author="name"<br>
- git shortlog / git shortlog -sn<br>
- git log --graph<br>
- git show (hash)<br><br><br><br><br>

- git revert (hash) # reverte para o historico anterior sem perde o commmit<br>
- git rebase (file)<br><br><br><br>




- .gitignore - arquivo na pasta do repo usada para ignorar arquivos que você não queira fazer commit


