<h2> align="center">
	🖥️ <br>Estudos sobre git
 </h2>

  [![NPM](https://img.shields.io/npm/l/react)](https://github.com/nandajfa/estudo_git/blob/main/LICENSE)


### Sistemas de controle de versão

* Sistemas capazes de registrar alterações em um conjunto de documentos de qualquer natureza.
* Podem ser imagens, aquivos de texto, arquivos de linguagens de programação.
* Armazenam um histórico que contém todas as alterações do projeto.
* Tudo fica registrado e você consegue retornar para versões anteriores.
* Permite que membros de um projeto trabalhem no mesmo documento ao mesmo tempo de forma isolada uns dos outros.

### Index

- [Seção 1 | Plataformas - Comandos - Configurações iniciais - Alias 💡](#seção-1)
- [Seção 2  📝](#how-to-use)
- [Seção 3 ⬇️ ](#what-are-the-commit-types)
- [Recommendations ☑️](#recommendations)
- [Emoji patterns 📍](#emoji-patterns)
- [References 🔗](#references)
- [Author Info  ✒️](#author)

---

## Seção 1

### Plataformas de hospedagens mais comuns

* Github
* Bitbucket
* Gitlab

### Comandos

* git init (criar repositório local no diretório) Cria a pasta .git(oculta) dentro dela estará o repositório.
* git remote add origin https://github.com/nandajfa/git.git (Conectar repositório remoto com local)
* git remote get-url origin

### Configurações iniciais

1- Definir nome e email que será exibido nos commits.

* git config [--local | --global | --system] <key> [<value>]
	--system: aplica as configurações para todo repositório de todos os usuários no seu computador.
	--global: aplica para todo repositório do usuário corrente.
	--local: aplica para o repositório corrente.

PS: As configurações serãp aplicadas na seguinte ordem:
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

---

 ### Author

Made by jessica Fernanda 👋 [See my linkedin](https://www.linkedin.com/in/jessica-fernanda-alves-marques-106651205/)


<br>[🔝 Back To The Top](#estudos-sobre-git-) <br>