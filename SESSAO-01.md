# Comandos básicos de git

O Git é um sistema de controle de versão distribuído, o que significa que um clone local do projeto é um repositório de controle de versão completo. Esses repositórios locais totalmente funcionais facilitam o trabalho offline ou remoto.

## Lista de comandos

### Trabalhando com Branches

<ul>
    <li>git branch <nome-da-branch></li>
    <li>git checkout <nome-da-branch></li>
    <li>git checkout -b <nome-da-branch></li>
    <li>git branch</li>
    <li>git branch -d <nome-da-branch></li>
</ul>

### Fluxo de Trabalho Básico

<ul>
    <li>git add nome_arquivo ou git add .</li>
    <li>git commit -m "mensagem do commit"</li>
    <li>git status</li>
    <li>git log</li>
    <li>git push</li>
</ul>

### Operações úteis

<ul>
    <li>git stash</li>
    <li>git stash apply</li>
    <li>git stash list</li>
    <li>git log</li>
    <li>git status</li>
</ul>

### Extensões do VS Code

<ul>
    <li><a href="https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens">GitLens</a></li>
    <li><a href="https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph">Git Graph</a></li>
</ul>

## Exercício

<ol>
    <li>Criar o arquivo “primeiro.txt” na branch main com a primeira linha escrito “Meu primeiro commit” </li>
    <li>Fazer o commit </li>
    <li>Push desse arquivo para o repositório remoto.</li>
    <li>Criar uma branch chamada “develop” e criar o arquivo “segundo.txt” com a primeira linha escrita “Meu segundo commit”.</li>
    <li>Fazer o commit e o push desse arquivo para o repositório remoto.</li>
    <li>Abrir um pull request para branch main.</li>
    <li>Fazer o merge do código</li>
    <li>Observar o resultado no Github(remote) e local com o git graph</li>
</ol>

### Resolução

<ul>
    <li>Crie o repositório</li>
    <li>Faça o clone para local</li>
    <li>Crie o primeiro arquivo</li>
</ul>

```
git add .
git commit -m "meu primeiro commit"
git push --set-upstream origin main
```

<ul>
 <li>Crie uma nova branch e vá para ela</li>
</ul>

```
git branch -b develop
git checkout develop
```

ou

```
git checkout -b develop
```

<ul> 
    <li>Após criar o segundo arquivo</li>
</ul>

```
git add .
git commit -m "meu segundo commit"
git push --set-upstream origin develop
```

<ul>
    <li>Vá ao GitHub e abra um pull request de develop para a branch main</li>
    <li>Faça o merge e observe o resultado</li>
</ul>

_Para trazer as alterações de remore para local, digite o comando:_

```
git pull origin main
```
