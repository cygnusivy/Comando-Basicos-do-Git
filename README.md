# **Comandos básicos com  Git**

## **ÍNDICE**
### **1. Navegando entre pastas e diretórios**
1.1 Comandos `ls` e `dir`

1.2 Comandos `cd` e `cd ..`

1.3 Comandos `mkdir`, `move`, `rmdir`, `rm`, `touch` e `clear`
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
