# **Comandos básicos com  Git**

### Primeiros passos para utilizar o Git na sua máquina:
#### 1. Baixe o Git clicando [neste link](https://git-scm.com/) e execute-o na sua máquina
#### 2. Abra o Git Bash e defina um nome de usuário e email utilizando os seguintes exemplo:
```
git config --global user.name "Maria Silva"
git config --global user.email "maria.silva@email.com"
```

## **ÍNDICE**
### **1. Navegando entre pastas e diretórios**
1.1 Comandos `ls` e `dir`

1.2 Comandos `cd` e `cd ..`

1.3 Comandos `mkdir`, `mv`, `rmdir`, `rm` e `clear`
### **2. Clonando repositórios e realizando commits**
2.1 Comandos `git clone`, `git status`, `git init`, `git add`, `git  commit`
### **3. Criando repositório remoto**
3.1 Comandos `git remote add origin`,
### **4. Branch e Merge**
4.1 Comandos `git branch`, `git merge` e `git checkout`

4.2 Comandos `git log` e `git stash`
### **5. Compartilhando e atualizando projetos**
5.1 Comandos `git fetch`, `git push` e `git pull`

## **1. Navegando entre pastas e diretórios**
### **Comandos** `ls` e `dir`

#### `ls` -> `ls` é a abreviação de list command, sendo utilizado para listar os arquivos e pastas que se encontram em um dado diretório, basta digitar `ls` no terminal que os diretórios serão listados. Este comando lista o diretório de uma forma que é possível acessá-los diretamente de dentro do terminal, sendo redirecionado ditetamente para o local onde o arquivo encontra-se dentro da máquina. Para isso, basta apertar a tecla `Ctrl` e clicar com o mouse em cima dos diretórios que, geralmente, estão marcados com cores especiais, diferentemente da forma como são listados com o comando `dir`.

#### `dir` -> Assim como o comando `ls`, o comando `dir` também lista o o conteúdo dos diretórios, mas distinguem em algumas aspéctos na forma como são exibidos os resultados no terminal.

#### De modo geral, a saída padrão do comando `ls` é um terminal que lista nomes de arquivos em colunas classificadas vertivalmente (da mesma forma que o comando `ls -C` faz). Contudo, quando a saída padrão não é um terminal (pode ser um arquivo), `ls` lista o nome de arquivos um por linha, do mesmo modo que o comando `ls -1` faz.
#### Agora, no caso da saída com o comando `dir`, que possui a saída na forma de terminal como padrão, este comando lista nomes de arquivos em colunas classificadas verticalmente, da mesma forma que o comando `ls -C`. [Clique aqui](https://sobrelinux.info/questions/7004/difference-between-dir-and-ls-terminal-commands#:~:text=Se%20eu%20digitar%20dir%20%2C%20ele,e%20pastas%20e%20arquivos%20ocultos.) saber mais sobre as particularidades dos comando `ls` e `dir`.

### **Comandos** `cd` e `cd ..`

#### `cd` é a abreviação para change directory, sendo utilizado para navegar entre os diretórios e pastas, ou seja, com o comando `cd` é possível entrar em um dado diretório. Sua aplicação é bem simples, basta digitar `cd NomeDoDiretório` ou `cd LocalDoDiretório` para conseguir entrar e conseguir acessar o conteúdo do mesmo. A navegação das entre os diretórios deve respeitar a regra de que uma dada pasta deve estar na pasta atual para poder ser acessad. Por exemplo, se ná sua máquina há um diretório **A** e dentro de **A** há a pasta **B** que por sua vez possui a pasta **C**, não é possível entrar na pasta **C** antes de acessar o conteúdo da **B**. Nesta situação seria necessário, estando dentro da pasta **A**, digitar o comando `cd B` e, já dentro de **B**, digitar o comando `cd C` para conseguir acessar seu conteúdo. 
#### Já com o comando `cd ..` é possível regressar para um dado diretório. Por exemplo, se você está no diretório **B** e quer voltar para o **A**, basta digitar no terminal `cd ..`

### **Comandos** `mkdir`, `mv`, `rmdir`, `rm`, `touch` e `clear`

#### `mkdir` é um comando básico utilizado para criar diretórios e subdiretórios. Por exemplo, no diretório onde deseja-se criar a pasta **documentos**, basta rodar o comando `mkdir documentos` que a pasta **documentos** será criada. 
```
mkdir documentos
```
#### O comando `mv` é utilizado para mover um arquivo de um diretório para outro, sendo utilizado da seguinte forma:
```
mv NomeDoArquivo NomeDoDiretórioDestino
```
#### Por exemplo, caso você queria mover a pasta **workspace** para o diretório **C:**, basta seguir o modelo apresentado anteriormente, da seguinte forma: 
```
mv workspace C:
```
#### `rmdir` é o comando utilizado para remover diretórios vazios. De modo geral, sua sintáx no terminal do Windows é:
```
rmdir DiretórioASerDeletado
```
#### Contudo, caso haja arquivo ou outros diretórios dentro deste diretório, o comando não é executado. Neste caso o comando `rm -R NomeDoDiretório` serve para este próposito, pois a flag -R é uma instrução recursiva que remove os arquivos de cima para baixo, excluindo tudo que há dentor do diretório. A flag `-r` pode substituir a flag `-R` e funciona da mesma maneira. É válido ressaltar que a partir do momento que o comando rm é executado não é possível recuperar os arquivos novamente.

#### `clear` é o comando utilizado para limpar o terminal, muito útil para aqueles que gostam de utilizar o terminal sempre limpo ou com pouco código. Basta rodar o comando `clear` no terminal que tudo que foi realizado anteriormente a este comando será retirado do terminal.

## **2. Clonando repositórios e realizando commits**
### **Comandos** `git init`, `git clone`, `git status`, `git add`, `git  commit`

#### O comando `git init` é utilizado para inicilizar um repositório do Git, podendo ser utilizado para converter um repositório existente e não versionado em um repositório d Git ou inicializar um repositório vazio. A utilização deste comando é primordial e deve ser aplicada como primeiro comando ao iniciar um novo projeto, pois a maioria dos outros comandos do git ficam indisponíveis fora de um repositório inicializado. Ao executar o comando `git init`, um subdiretório .git no diretório de trabalho atual é criado, este diretório contém todos os metadados Git necessários para o novo repositório. Para executar o comando `git init` basta entrar no subdiretório do pprojeto e executar `git init`. 

#### `git clone` também pode ser aplicado para inicializar um repositório. Porém o `git clone` é um comando dependente do `git init`, sendo utilizado para criar uma cópia de um repositório existente no repositório de destino. Ao rodar o `git clone` no terminal de comando do Git, o comando `git init` será chamado primeiramente, criando assim um novo repositório. Em seguida, copia os dados do repositório existente e faz checkout de um novo conjunto de arquivos de trabalho. A padrão utilizado para clonar um repositório é mostrado abaixo:
```
git clone 'https://github.com/cygnusivy/Comando-Basicos-do-Git.git'
```
#### O exemplo acima demonstra como obter uma cópia local do repositório central armazenado no servidor acessível em https://github.com/cygnusivy/Comando-Basicos-do-Git.git 

#### Em seguida, o comando `git status` pode ser utilizado para ver se houve alguma alteração no código ou se houve alguma mudança qualquer nas pastas e arquivos do repositório local. Basta executar o comando `git status` dentro do diretório atual que que um resumo das alterações será exibido no terminal. As flags `-s` e `-v` podem ser aplicadas ao `git status` para que as alterações possam ser visualizadas de outra forma. O comando `git status -s` retorna as alterações em formato mais curto, ao passo que `git status -v` retorna as alterações de forma mais detalhada, inclusive as alterções dentro do código. Para mais finformações sobre `git status` [Clique aqui](https://git-scm.com/docs/git-status)
