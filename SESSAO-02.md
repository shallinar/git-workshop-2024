# Colaboração com git

Nesta sessão exploramos como usar git com GitHub para contribuir para projetos.

Falamos de como criar Pull Requests e como resolver _merge conflicts_.

### Criação de Pull Request

1. Fork do projeto para o qual queres contribuir
2. Clona o teu fork com `git clone <link-do-teu-fork>` no teu ambiente local
3. Cria o branch com `git checkout -b <nome-do-branch>`
4. Faz as alterações...
5. Adiciona as tuas alterações com `git add .`
6. Cria um commit com `git commit -m "<msg>"`
7. Faz push com `git push`
8. No teu repositório Fork, ou o original procura a caixinha de sugestão de criação de PR, e clica no botão verde
9. Verifica que o base branch é o branch princinpal (ex. `main`) e o repositório base, é o original (em vez do teu Fork)
10. E voilá!


### Commandos a usar

Estes são alguns comandos relevantes para gerires coleborações, diferentes branches e _merge conflicts_.
```
git checkout main
git pull
git checkout <branch_local_que_pretendes_atualizar>
git merge origin/main
git status
git add .
git commit <…>
git push
```

mais especificamente...

- `git checkout <branch>` para mudar para o branch `<branch>`
- `git pull` para atualizar o teu código local, com o código mais atualizado no repositório remoto
- `git merge origin/<branch-com-atualizacoes>` incorpora as modificações do branch `<branch-com-atualizacoes>` (remoto) no teu branch atual `<branch>`
- `git merge <branch-com-atualizacoes>` incorpora as modificações do branch `<branch-com-atualizacoes>` (local) no teu branch atual `<branch>`
- `git add .` adiciona todos os ficheiros com modificação, em preparação para fazer parte de um _commit_
- `git commit -m <msg>` cria um commit com a versão atual do código, com os ficheiros que foram preparados com `git add .`
- `git push` atualiza o reporitório remoto, com os teus novos commits locais 

### Como resolver _merge conflicts_

Se quiseres **incorporar uma modificação do repositório original** podes fazer o seguinte:
1. Atualiza o teu repositório Fork com o código do repositório original (GitHub disponibiliza um botão "Sync fork" -> "Update branch" que podes usar na página principal do teu fork)
2. Localmente, muda pra o branch principal com `git checkout main` (assumindo que `main` é o branch, em vez de por exemplo `dev` ou `master`)
3. Atualiza esse branch com `git pull`
4. Muda o teu branch com `git checkout <teu-branch>`
5. E faz _merge_, i.e., incorpora as modificações do branch `main` no teu branch com `git merge main`.

Aqui pode correr tudo bem, e não teres conflitos...
Caso tenhas conflitos...

Podes resolvê-los...
1. Abrindo o teu editor de texto, e podes escolher qual o estado final do teu repositório, e adicionar as modificações como costumas fazê-lo:
2. Adiciona as tuas modificacoes com `git add .`
3. Faz commit com `git commit -m <msg-de-resolucao>`
4. Faz push com `git push`
5. Verifica na tua PR que já não tens conflitos no código


Nota: Há várias formas como podes gerir os branches usando git, estes passos é apenas uma forma :)

