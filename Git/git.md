<div align="center">
    <img src="https://github.com/andreubita/MIEI-resumos/blob/master/Git/img/git-github.png" align="center" alt="git-github">
    <strong><i>Git - GitHub</i></strong>
    <br>
    <br>
</div>

# Git vs GitHub
**Git**: é um sistema de controlo de versão, uma ferramenta que ajuda a manter um histórico do codígo.

**GitHub**: é uma plataforma que permite hospedar repositórios e permite a colaboração de diferentes membros.

# Git

### Instalar Git

###### Ubuntu
```
$ sudo apt-get install git
```

###### Windows
Download do [Git para Windows](https://git-scm.com/).

### Credenciais

É necessário definir um nome e um email para identificarem o autor dos commits.

```
$ git config --global user.name "nome"
$ git config --global user.email "email@uminho.pt"
```

### Criar um repositório
Um repositório (aka repo) é a versão Git de um projeto. O git irá detetar todas as mudanças que são feitas nele.

Para criar-mos um repositório dentro da pasta do projeto executamos o seguinte comando.

```
$ git init
```

### Estado
Consegui-mos saber o estado do nosso repositório com o seguinte comando.

```
$ git status
```

Os ficheiros podem estar:

- **Modified**: não são afetados pelo commit.
- **Staged**: estão à espera de commit.

### Commit
```
$ git add <ficheiro>
```
Serve para turnar um ficheiro **Modified** em **Staged**

```
$ git restore --staged <ficheiro>
```
Serve para turnar um ficheiro **Staged** em **Modified**

Para adicionar todos os ficheiros de uma vez podemos no lugar de `<ficheiro>` colocar um `.`.

Agora os ficheiros estão à espera de commit.
Para isso podemos executar o comando.

```
$ git commit -m "mensagem"
```

# GitHub

### Criar repositório

<img src="https://github.com/andreubita/MIEI-resumos/blob/master/Git/img/github-create-repo.png" align="center" alt="github-create-repo">

### Adicionar colaboradores
Para adicionar colaboradores basta ir às definições do repositório e na segunda secção clicar em adicionar colaboradores.

<img src="https://github.com/andreubita/MIEI-resumos/blob/master/Git/img/github-colab.png" align="center" alt="github-colab">

### Importar repositório
Depois de termos o repositório online criado pode-mos associar o nosso repositório no git com o do github criando um remote.

```
$ git remote add origin https://github.com/andreubita/hello-world.git
```
*Nota*: origin é o nome do nosso remote, pois pode-mos enviar o repositório para diferentes plataformas.
*Nota*: Adicionar .git no fim do link.

### Pull
Pull server para atualizar-mos o nosso repositório local com o GitHub.

```
$ git pull origin master
```

*Nota*: Após a execução de um pull é preciso executar um fetch

```
$ git fetch origin master
```

### Push
Push serve enviar-mos os nossos commits para o GitHub.

```
$ git push origin master
```

*Nota*: Caso um colaborador tenha atualizado o código no GitHub é necessário executar um pull antes.