# Aula 1
## **Sistema de trabalho**
 O git possui um sistema de trabalho que funciona em 3 blocos:

 #### **Diretorio de trabalho**
>Área referente ao dispositivo

 #### **Área de preparação**
>Área responsável por armazenar as alterações antes de ser enviado para o repositório

 #### **Repositório** 
 > Área onde ficam armazenados os códigos e arquivos do projeto 

 ![Sistema do Git](https://www.revista-programar.info/wp-content/uploads/2011/06/git-staging-area.png)

# 
## **Branch**
### **O que são:**
As branchs são como se fosse versões do codigo principal só que de um universo paralelo. Elas exisatem, são parecidas mas acontecem coisas diferentes com elas. Ou seja, as branchs são uma forma de você editar o código principal sem afetar ele.

Abaixo terá um exemplo:
![Branch](https://imgs.search.brave.com/I4g1MKkO2kmnfqfVZvZsuzRBFds3uWTbKOtLS0nXbWI/rs:fit:1200:1126:1/g:ce/aHR0cHM6Ly93d3cu/Y29kZXdhbGwuY28u/dWsvd3AtY29udGVu/dC91cGxvYWRzLzIw/MTkvMDUvU2NyZWVu/c2hvdC0yMDE5LTA1/LTMwLWF0LTE5LjQ1/LjE0LnBuZw)

### **Como usar:**
Elas podem ser criada atravez do comando `git checkout -b <nomeDaBranch>`. Esse comando, alem de criar a branch, ò leva para a para ela.

Para alternar entre branchs, pode ser usado o mesmo comando de cima, apenas tirando o `-b`, como o exemplo: `git checkout <nomeDaBranch>`

Até o momento, a branch está apenas no nosso repositorio local (maquina/pc), para enviar para o repositório remoto (nuvem), é preciso executar o seguinte comando: `git push --set-upstream origin <nomeDaBranch>`

Agora sua branch está no repositório remoto do git!!!

### **Como nomear**
Agora você pode estar se perguntando: "Como devo nomear minhas branchs?", "Existe um padrão para nomear?". A resposta é: Temos um padrão para nomea-las. A baixo está o padrão:

1. **docs:** Mudanças na documentação
1. **feat:** Nova funcionalidade
1. **fix:** Correção de um bug 
1. **perf:** Mudança do código visando o desempenho
1. **refactor:** Mudanças no código que nao alteram em funcionalidade ou bug 
1. **style:** Mudanças no estilo
1. **test:** Adiciona ou corrige os testes

# Aula 2
## **`git stash`**
Este comando é responsavel por armazenar os temporariamente os arquivos adicionados ou modificados em uma stash (esconderijo), sem interação com os outros arquivos até que seja nescessário. 

Para listar as stashs, basta executar o seguinte comando: `git stash list`

## **`git rebase`**
Este comando é utilizado para juntar multiplas branchs, assim como o comando `merge`, com a diferença de que o rebase pega todos os commits de cada branch e às organiza de forma linear, quanto o merge não, ele junta tudo em um unico histórico.
`git rebase `