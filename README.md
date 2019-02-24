# Anotações: comandos básicos do Git

<p align="center">
  <a href="https://pixabay.com/pt/papel-bagun%C3%A7ado-notas-abstract-3033204/" target="_blank" >
    <img alt="Notes" src="https://cdn.pixabay.com/photo/2017/12/22/08/01/paper-3033204_960_720.jpg" width="400" />
  </a>
</p>


Fonte: [Curso Básico de Git - RBtech](https://www.youtube.com/playlist?list=PLInBAd9OZCzzHBJjLFZzRl6DgUmOeG3H0) 


## Working Area

- Transformar a pasta local num repositório
``` bash
$ git init
```

- Remover o(s) arquivo(s) do repositório
``` bash
$ git rm nomeArquivo.ext
```

- Mostrar as alterações feitas no(s) arquivo(s) que estão na Working Area
``` bash
$ git diff
```

## Staging Area

- Adicionar o(s) arquivo(s) na Staging Area
``` bash
$ git add nomeArquivo.ext
```

- Retirar o arquivo da Staging Area
``` bash
$ git reset HEAD nomeArquivo.ext
```

- Fazer com que o(s) arquivo(s) volte(m) para o padrão que estava(m) na Staging Area.
``` bash
$ git checkout -- nomeArquivo.ext
```

- Mostrar as alterações feitas no(s) arquivo(s) que está(ão) na Staging Area
``` bash
$ git diff --staged 
```

## Commit

- Commit dos arquivos que estão na Staging Area para o respositório
``` bash
$ git commit -m "mensagem" 
```

- Editar o último commit
``` bash
$ git commit --amend -m "mensagem (edição")
```

- Exibir todos os commits realizados
``` bash
$ git log
```

- Exibir todos os commits realizados + os diffs
``` bash
$ git log -p
```

- Exibir uma quantidade específica de commits + os seus diffs
``` bash
$ git log -p -quantidade (ex: $ git log -p -2)
```

- Exibir os commits com seus comentários, sem maiores detalhes
``` bash
$ git log --pretty=oneline
```

- Abrir o visualizador de histórico de commits (GUI)
``` bash
$ gitk
```

## Branch

- Cria uma branch
``` bash
$ git branch nomeBranch
```

- Acessar a branch
``` bash
$ git checkout nomeBranch
```

- Apagar a branch
``` bash
$ git branch -d nomeBranch
```

- Adicionar as modificações da branch fonte na branch corrente (master ou outras)
``` bash
$ git merge branchFonteArquivos
```

- Listar as branchs existentes
``` bash
$ git branch
```

- Conflitos entre branchs 
Verificar a(s) linha(s) onde ocorre o conflito e resolvê-lo manualmente.

## Conexão com o GitHub

- Gerar a keygen
	Deixar sem senha, caso contrário, será necessário informá-la a cada push/pull
	Entrar na pasta onde estão as chaves e abrir o .pub. É neste arquivo que encontra-se a chave.
	GitHub: acessar settings -> SSH and GPG Keys -> New SSH key -> colar a key no local apropriado

``` bash
$ ssh-keygen
```

- Clonar o repositório do GitHub (faz o download dos arquivos para uma pasta local)
	
	O link para clone está disponível em cada repositório no GitHub

``` bash
$ git clone enderecoRepositorioGit (nomeRepositorioLocal "opcional")
```
 	

- Push (envio) dos arquivos commitados para o GitHub

	Obs: verificar se estais no repositório correto antes de fazer o push

``` bash
$ git push origin master
```
	

- Pull (pega) dos arquivos commitados no GitHub

	Obs: verificar se estais no repositório correto antes de fazer o pull

``` bash
$ git pull origin master
```
	

## Outros

- Limpar a tela
``` bash
$ clear
```