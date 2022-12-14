### **Seção 2**
___
<br>

### Três áreas importantes

* *Área de trabalho*: contém os próprios arquivos fisicos e diretórios que você visualiza e altera.
* *Staging*: Zona do próximo commit. Tudo que estiver nela será adicionado no commit que for realizado.
* *Repositório*: Contém os arquivos que o git conhece e todo o histórico de commits do projeto.

**Commits** -> Versões do seu projeto. Você pode retornar para qualquer versão anterior facilmente.

### Primeiro commit

```
$ echo "hello world" > hello.txt

$ git add hello.txt #ou
$ git add .

$ git commit -m "Creating hello.txt"

$ git hist

$ git log
```

* Área de staging ou área de preparo (Contém todas os arquivos e alterações que serão considerados no commit)

<img src="img/stage.png">

---

### Git Show

* Para visualizar as alterações em um determinado commit, pode ser utilizado o comando git show.

```
$ git show

$ git show <commit(hash N)...<commit(hash)M> #mostrar alterações de um conjunto de commits

```

### Git push

* Empurrando notificações para o servidor remoto

```
$ git push
#msg de erro = Branch master local ainda não possui uma branch de rastreamento.

$ git push --set-upstream origin master

```

### Git ids

* Git id é o nome de um objeto git
* No primeiro commit é gerado uma string de 40 caracteres que é o identificador desse commit.
* O comando 'git log' mostrará essa string de 40c. Essa string é o nome de um objeto de commit (contido em .git/objects)
* No 'git hist' aparece os primeiros 7 caracteres.

<img src="/img/sha1.png">

```
$ git log

$ git hist
```

### Git objects

* Dentro de um repositório raiz do git podemos ter arquivos e diretórios. Diretórios que geralmente contém outros diretórios.
* No git o conteúdo dos arquivos são armazenados em objetos chamados **Blobs**.
* Diretórios são equivalentes a uma árvore.(**tree**)
   -> Uma árvore é basicamente uma lista de diretórios referindo-se a blobs, bem como a outras árvores.
* Um commit é uma imagem (snapshot) desse sistema de arquivos em um determinado momento.

```
$ git hist

$ git cat-file -t <hash do primeiro commit>
$ git cat-file -p <hash do primeiro commit>
# identificador da árvore

$ git cat-file -t <hash da árvore>
$ git cat-file -p <hash da árvore>
#aparece o identificador do blob

$ git cat-file -t <hash do blob>
$ git cat-file -p <hash do blob>
# o que contém no arquivo

```

<img src="/img/objects.png">

```
$ mkdir docs
$ cd  docs
$ echo "orientacoes" > orientacoes.txt
$ echo "pendencias" > pendencias.txt
$ git add .
$ git commit -m "creating docs"
```

<img src="/img/tree.png">

<img src="/img/tr.png">

### Clonando um repositório remoto

* O git clone vai realizar uma cópia do repositório remoto e configurá-lo automaticamente como uma pasta GIT (internamente ele executa um git init).
* O git clone também executa um *git fetch*.
* Sendo assim, já existe uma *branch de rastreamento* master do remote origin que rastreia nossa *branch local master*.
* Se tiver alguma alteração para empurrar, bastaria um *git push*.

<img src="/img/clone.png">

```
$ git clone <URL do reposiório>
```

### Status dos arquivos

* Exibe um relatório mostrando os arquivos que foram alterados ou criados e que ainda não foram comitados.

```
$ git status
```
<img src="/img/unt.png">

**Status Untracked** -> Esse arquivo ainda não está sob o controle do git.

<img src="/img/status.png">

```
$ git add .
$ git status
```
<img src="img/staged.png">

```
$ git commit -m "<mensagem>"
$ git push
```
