<div align="center"> 
  
  <h1> Git - tutorial  </h1>
  <img src="https://img.icons8.com/nolan/64/git.png"/>

</div>

#  Noções básicas do Git


O objetivo deste Git tutorial é apresentar alguns dos principais comandos que você precisa para começar a usar o Sistema de Controle de Versão Distribuído. Além de ser distribuído, o Git foi projetado com desempenho, segurança e flexibilidade em mente. O Git é muito capaz e disponibiliza muitos recursos aos usuários. Aprender a usar esses recursos pode levar algum tempo. No entanto, uma vez aprendidos, podem ser usados pela equipe para aumentar a velocidade de desenvolvimento.





# 📑Documentação

[https://git-scm.com/book/en/v2](https://git-scm.com/book/en/v2)


[O que é o Git.](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F)

[Instalando o Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

[Como o Git funciona.](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)



<div align=""> 
  
  <h1> 🗺 Git map comandos </h1>
  <h1> 
  <img src="https://user-images.githubusercontent.com/85380530/141888420-847895fe-f1e1-4440-a06e-7ebcb00a1648.PNG" height="400" width="800"/>
</div>




# **Conteúdo**

- **O que é o Git**
- **Como o Git funciona**
- **Instalando o Git em sistemas diferentes**
    - **I**nstalando no Linux
    - Instalando no Mac
    - Instalando no Windows
- **Principais comandos Git**
    - Git init
    - Git clone
    - Git branch
    - Git checkout
    - Git status
    - Git add
    - Git commit
    - Git push
    - Git pull
    - Git revert
    - Git merge
- **Conclusão - tutorial Git**

# **O que é o Git**



O Git é um sistema de controle de versão gratuito e de código aberto criado por Linus Torvalds em 2005. Diferente de outros sistemas de controle de versão centralizados, como SVN e CVS, o Git é um sistema distribuído, significa que cada diretório de trabalho do Git é um repositório com um histórico completo e habilidade total de acompanhamento das revisões, independente de acesso a uma rede ou a um servidor central. Ele é usado principalmente no desenvolvimento de software, mas pode ser usado para registrar o histórico de edições de qualquer tipo de arquivo.

# Como o Git funciona

<div align=""> 
  
  <h1> 
  <img src="https://user-images.githubusercontent.com/85380530/141887774-e676b544-668a-435f-ad1b-949ecd4605f2.png" height="400" width="800"/>
</div>


Aqui está uma visão geral básica de como o Git funciona:

1. Crie um "repositório" (projeto) com uma ferramenta de hospedagem de git (como o GitHub).
2. Copie (ou clone) o repositório na sua máquina local.
3. Adicione o arquivo ou seu repositório local e faça "commit" (salve) as alterações.
4. "Coloque" suas alterações na sua ramificação principal.
5. Faça uma alteração no seu arquivo com uma ferramenta de hospedagem de git e faça commit.
6. "Puxe" as alterações para a sua máquina local.
7. Crie uma "ramificação" (versão), faça uma alteração, faça commit da alteração.
8. Abra uma "solicitação pull" (proponha alterações na ramificação principal).
9. "Mescle" sua ramificação com a principal.

# Instalando o Git

## **Instalando o Git em sistemas diferentes**

### **Instalando no Linux**

Se você deseja instalar o Git no Linux através de um instalador binário, você pode geralmente fazê-lo através da ferramenta básica de gerenciamento de pacotes que vem com sua distribuição. Se você usar Fedora por exemplo, você pode usar o yum:

```sh 
$ sudo yum install git-all
```

Se você usar uma distribuição baseada em Debian como o Ubuntu, use o apt-get:

```sh 
$ sudo apt-get install git-all
```

Para mais opções de instruções de como instalar o Git em outros vários sistemas Unix, veja na página do Git, em [http://git-scm.com/download/linux](http://git-scm.com/download/linux).

### **Instalando no Mac**

Existem várias maneiras de instalar o Git em um Mac. O mais fácil é provavelmente instalar as ferramentas de linha de comando Xcode. No Mavericks (10,9) ou acima, você pode fazer isso simplesmente rodando ***git*** a partir do Terminal pela primeira vez. Se você não tiver o Git instalado, ele irá pedir-lhe para instalá-lo.

Se você quiser uma versão mais atualizada, você também pode instalá-lo através de um instalador binário. Um instalador OSX Git é mantido e disponível para download no site do Git, pelo [http://git-scm.com/download/mac](http://git-scm.com/download/mac).

### **Instalando no Windows**

Há também algumas maneiras de instalar o Git no Windows. A compilação mais oficial está disponível para download no site do Git. Basta ir ao [http://git-scm.com/download/win](http://git-scm.com/download/win) e o download começará automaticamente. Note que este é um projeto chamado Git para Windows (também chamado msysGit), que é algo separado do Git; para mais informações sobre isso, vá para [http://msysgit.github.io/](http://msysgit.github.io/).

Para fazer uma instalação automatizada, você pode usar o [pacote Git do Chocolatey](https://chocolatey.org/packages/git). Note que o pacote Chocolatey é mantido pela comunidade.

# Principais comandos Git

## Git init

O comando ```git init``` você utilizará para começar um projeto que ainda não seja um repositório, este comando irá criar um repositório vazio ou transformar uma pasta que você já tem, e que não está com controle de versão, em um repositório. 

```sh 
$ git init
```

## Git clone

O comando ``` git clone ``` irá baixar o código-fonte existente de um repositório remoto como o Github, por exemplo, existe outras maneiras de baixar o código-fonte esta é apenas uma delas.

 ```sh 
 $ git clone <https://url-do-link>
 ```

O código será copiado para a sua máquina e continuará linkado ao original, para desvincular a sua cópia do original,  você irá rodar o comando:

```sh 
$ git remote rm origin
```

## **Git branch**

Com ramificações vários desenvolvedores podem trabalhar paralelamente no mesmo projeto, cada um pode codar a sua parte sem ter problemas no projeto, sendo este um dos comandos Git mais importantes. 

O comando ``` git branch ``` pode ser usado para criar, listar e excluir branches.

Criando uma nova branch:

```sh 
$ git branch <nome-da-branch>
```

O comando criará uma *branch* local. Para subir a nova *branch* para o repositório remoto, você pode usar o comando:

```sh
$ git push -u <remote> <nome-da-branch>
```

Utilize os comandos para ver as ramificações:

```sh 
$ git branch
```  

ou 

```sh 
$ git branch --list
```

Para deletar um branch você utilizará o comando:

```sh 
$ git branch -d <nome-da-branch>
```

# **Git checkout**

O comando ``` git checkout ``` irá alternar de um *branch* para outra e também poderá ser usado para restaurar arquivos de árvore de trabalho:

```sh 
$ git checkout <nome-da-ramificação>
```

O comando ``` git checkout -b ``` permite criar e ir para um branch direto:

```sh 
$ git checkout -b <nome-da-branch>
```

# Git status

O comando ``` git status ``` trás informações sobre a *branch* em que você estiver no momento, como seu nome, se ela está atualizada em relação à master e quais arquivos foram alterados.

```sh 
$ git status
```

# Git add

Este comando atualiza o índice usando o conteúdo atual encontrado na árvore de trabalho, para preparar o conteúdo testado para o próximo commit. Normalmente adiciona o conteúdo atual de caminhos existentes como um todo, mas com algumas opções também pode ser usado para adicionar conteúdo com apenas parte das alterações feitas nos arquivos da árvore de trabalho aplicados ou remover caminhos que não existem na árvore de trabalho mais.

Comando para adicionar apenas um arquivo:

```sh 
$ git add <aqrquivo>
```

Comando para adicionar todos os arquivos modificados:

```sh 
$ git add -A
```

O comando ```git add ``` não altera o repositório e as alterações não são salvas até usarmos o comando ``` git commit```.

# Git commit

Grava alterações no repositório, cria um novo commit contendo o conteúdo atual do índice e a mensagem de log fornecida descrevendo as mudanças.

```sh 
$ git commit -m "mensagem explicando a mudança no código"
```

# Git push

Atualiza referências remotas junto com objetos associados, envia a ramificação especificada para , junto com todos os commits e objetos internos necessários, criando uma ramificação local no repositório de destino.  

O comando ``` git push ``` envia e salva as confirmações no repositório remoto:

``` sh 
$ git push <remote> <nome-do-branch>
```

Para fazer upload da branch criada recentemente será utilizado o seguinte comando:

```sh 
$ git push -u origin <nome-do-branch>
```

# Git pull

O comando `git pull` é usado para buscar e baixar conteúdo de repositórios remotos e fazer a atualização imediata ao repositório local para que os conteúdos sejam iguais. Fazer o merge de alterações upstream remotas no repositório local é algo comum em fluxos de trabalho de colaboração baseados em Git. O comando `git pull` é a combinação de dois outros comandos, o `[git fetch](https://www.atlassian.com/br/git/tutorials/syncing/git-fetch)`, seguido do `[git merge](https://www.atlassian.com/br/git/tutorials/using-branches/git-merge)`. No primeiro estágio da operação, o `git pull` executa o comando `git fetch`, que abrange a ramificação local para qual a `HEAD` aponta. Quando o conteúdo é baixado, o `git pull` insere o fluxo de trabalho de merge. O commit de merge é criado e a `HEAD` é atualizada para apontar o novo commit.

Opções comuns 

```sh 
$ git pull <remote>
```

Busque a cópia remota especificada da ramificação atual e faça o merge de imediato na cópia local. É o mesmo que `git fetch ＜remote＞` seguido de `git merge origin/＜current-branch＞`.

```sh 
$ git pull --no-commit <remote>
```

Semelhante à invocação padrão, obtém o conteúdo remoto, mas não cria um novo commit de merge.

```sh 
$ git pull --rebase <remote>
```

Igual ao pull anterior. Em vez de usar `git merge` para integrar a ramificação remota com a local, use `[git rebase](https://www.atlassian.com/br/git/tutorials/rewriting-history/git-rebase)`.

```sh 
$ git pull --verbose
```

Oferece uma saída especificada durante uma extração que exibe o conteúdo que está sendo baixado e os dados de merge.

# Git revert

O comando `git revert` é uma operação de desfazer avançada que oferece um método seguro de desfazer alterações. Em vez de excluir ou tornar commits órfãos no histórico de commits, uma reversão vai criar um commit novo que inverte as alterações especificadas.

Desfazendo  os *commits*  usando `git revert`:

```sh 
$ git revert `numero do hash
```

Comando para ver o número do hash:

```sh 
$ git log -- oneline
```

# Git merge

Mesclagem é o jeito do Git de unificar um histórico bifurcado. O comando `git merge` permite que você pegue as linhas de desenvolvimento independentes criadas pelo `git branch` e as integre em uma ramificação única. Quando o desenvolvimento da sua branch funciona sem conflitos, a etapa final é mesclar as *branches*, feito com o comando `git merge`.

Para mesclar todas as alterações feitas em seu repositório local irá usar o comando:

```sh 
$ git merge <nome-da-branch>
```

# Conclusão - Git tutorial

Vale ressaltar que existe diversas outras opções de comandos e configurações, este tutorial trás noções básica do Git, irá ajudar a qualquer desenvolvedor a utilizar os comandos  básicos do Git, sendo um sistema de controle de versão com uma infinidade de recursos, para saber mais sobre o Git consulte a [documentação do Git](https://git-scm.com/book/en/v2).

# ✏ Contribuições  
  
Sinta-se a vontade para:
  
- Fazer um fork
- Adicionar informações


