# Anotações: comandos básicos do Git

<p align="center">
  <a href="https://pixabay.com/pt/papel-bagun%C3%A7ado-notas-abstract-3033204/" target="_blank" >
    <img alt="Notes" src="C:\Users\alyss\Desktop\git-learning\pixabay-paper-3033204_640.jpg" width="400" />
  </a>
</p>


Fonte: [Curso Git para Iniciantes - RBtech](https://www.youtube.com/playlist?list=PLInBAd9OZCzzHBJjLFZzRl6DgUmOeG3H0) 


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



## Outros
- Limpa a tela
``` bash
$ clear
```

