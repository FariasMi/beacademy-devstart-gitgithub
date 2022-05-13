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
**Gravar alterações realizadas no workflow**

Para que seja possível gravar as alterações realizadas no workflow de versionamento do github, gerar logs de alteração e "preparar" as alterações para serem incluídas no repositório remoto, é necessário executar o seguinte comando:
```git commit
$ git commit -m "uma descrição sucinta e clara sobre as alterações realizadas"
```
