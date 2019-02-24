# Anotações: comandos básicos do Git

<p align="center">
  <a href="https://pixabay.com/pt/papel-bagun%C3%A7ado-notas-abstract-3033204/" target="_blank" >
    <img alt="Notes" src="pixabay-paper-3033204_640.jpg" width="400" />
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

conflitos entre branchs 
verificar a linha onde há conflito no arquivo e commitar com o conflito resolvido manualmente

## Outros
- Limpa a tela
``` bash
$ clear
```

## Conexão com o GitHub

$ ssh-keygen : gera a key
	- deixar sem senha
	- abrir a pasta onde estão as chaves e abrir o .pub
	- no github: acessar settings -> SSH Keys -> colar a key no local apropriado

$ git clone enderecoRepositorioGit (nomeRepositorioLocal "opcional") : clona o repositório do github
 	- o link para clone é disponibilizado no github

$ git push origin master : enviar os arquivos comitados para o github
	- verificar se está no repositório correto antes de enviar

$ git pull origin master : pegar os arquivos comitados no github
	- verificar se está no repositório correto antes de fazer o comando