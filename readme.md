## Comandos e uso 

**Sua identidade**

A primeira coisa que você deve fazer ao instalar o Git é definir seu nome de usuário e endereço de e-mail. 

Isso é importante porque todo commit do Git usa essa informação e é imutavelmente incorporada aos commits que você começa a criar:
```git config
$ git config --global user.name "seu nome"
$ git config --global user.email [seu email]
```
**Inicializando o repositório**

Para que seja possível a utilização do github em sua máquina local, é necessário transformar o diretório local em um repositório local. Com este comando, é possível iniciar um repositório vazio em seu diretório ou reinicializar um existente:
```git init
$ git init
```
**Status do workflow**

Após criar ou editar arquivos dentro do repositório, é possível consultar em qual momento do workflow este arquivo se encontra, assim como arquivos que não estão rastreáveis:

```git status
$ git status
```
**Adicionar arquivo(s) ao workflow**

Para tornar o arquivo rastreável, ou seja, permitir que este arquivo faça parte do workflow de versionamento do github, é necessário executar o seguinte comando:

```git add
// inclui todos os arquivos criados no repositório e ainda não rastreados
$ git add .

// Permite rastrear um arquivo específico
$ git add <nome do arquivo>
```
**Excluir remover um arquivo do workflow**

Ao tornar um arquivo rastreável, é possível desfazer a ação, ou seja, retirá-lo do workflow de versionamento:
```git rm 
$ git rm --cached <nome do arquivo>
```
**Criando ramificações(branches)**

Em um mesmo repositório, é possível criar ramificações(branches) dentro do workflow, ou seja, criar subfluxos capazes de serem trabalhados paralelamente sem um afetar o outro diretamente, até que sejam unificados:

```git branch
//Consulta todas as branches criadas no repositório
$ git branch

//Cria uma nova branch
$ git branch <nome_da_branch>
```

**Trocando de branch**

Assim como é possível a criação de inumeras branches dentro de um mesmo workflow, é possível também navegar entre elas:

```git checkout
//Trocar de branch
$ git checkout <nome_da_branch>

//Cria uma branch e torná-la a branch atual
$ git checkout -b <nome_da_branch>
```

**Removendo uma branch**

É possível também remover a branch do repositório:
```git branch -d
$ git branch -d <nome_da_branch>
```
**Gravar alterações realizadas no workflow**

Para que seja possível gravar as alterações realizadas no workflow de versionamento do github, gerar logs de alteração e "preparar" as alterações para serem incluídas no repositório remoto, é necessário executar o seguinte comando:
```git commit
$ git commit -m "uma descrição sucinta e clara sobre as alterações realizadas"
```

**Consultar os commits realizados no repositório**

Para consultar os commits realizados no repositório:
```git log
$ git log
```
**Salvando as alterações no workflow antes do commit**

Com o stash, é possível salvar as alterações no workflow, que já foram rastreadas, temporariamente, para poder trabalhar em outras ramificações, por exemplo. Esta funcionalidade não substitui o commit e pode ser utilizadas em momentos que se é necessário alterar um subfluxo de trabalho (branch), sem perder a atual:
```git stash
//Para incluir arquivos não rastreados
$ git stash --include-untracked

//Para salvar as alterações sem os arquivos não rastrados
$ git stash

//Para listar todos os "stashs" feitos no repositório
$ git stash list

//Para recuperar um stash 
$ git stash pop [nome do stash]
```


## Referências

 - [Pra entender o workflow do git](https://github.com/PauloGoncalvesBH/treinamento-git)
 - [Documentação git](https://git-scm.com/docs/git-branch)
 - [Treinamento Be academy](https://www.beacademy.com.br/)