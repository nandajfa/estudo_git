
## Seção 1

### Plataformas de hospedagens mais comuns

* Github
* Bitbucket
* Gitlab

<img src="/img/pl.png"><br>

### Comandos

* git init (criar repositório local no diretório) Cria a pasta .git(oculta) dentro dela estará o repositório.
* git remote add origin https://github.com/nandajfa/git.git (Conectar repositório remoto com local)
* git remote get-url origin

### Configurações iniciais

1- Definir nome e email que será exibido nos commits.

``` git config [--local | --global | --system] <key> [<value>] ```

*	--system: aplica as configurações para todo repositório de todos os usuários no seu computador. <br>
	--global: aplica para todo repositório do usuário corrente. <br>
	--local: aplica para o repositório corrente. <br>

PS: As configurações serão aplicadas na seguinte ordem:
* Caso tenha local, prevalece local.
* Caso tenha global, prevalece global.
* Se não, prevalece a do sistema.

Exemplo:

```
$ git config --global user.name "<SEU NOME>"
$ git config user.name
$ git config --local user.name "<SEU NOME>"
$ git config --local user.email "<SEU EMAIL>"
$ git config user.name
```
### Aliases

* O termo Alias é sinônimo de Atalho.
* Usados para criar comandos menores que correspondem a comandos maiores.
* Fluxos de trabalho mais eficientes.

Exemplo:

```
git config [--local | --global | --system] alias.<comando curto> <comando longo>

# log (histórico de commits)
# atalho hist

$ git config --global alias.hist 'log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short'
```

### Ajuda

* Acessar o manual do git

```
$ git <verb> --help
```