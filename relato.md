
# Relatório de Introdução ao Linux usando Docker no Windows
Nome: Asaph Arruda
Data: 10/05/2025

## Introdução
O objetivo desse exercício foi praticar comandos básicos do Linux dentro de um contêiner Docker usando a imagem do Fedora. A ideia principal era aprender, testar e entender o funcionamento desses comandos em um ambiente controlado.

## Relato

### 1. Iniciar um contâiner Fedora
Inicialmente, utilizando o comando abaixo, nós criamos o container com a imagem do Fedora

```
docker run -it --name fedora-tutorial fedora:latest /bin/bash
```
![imagem de exemplo](imgs/01-img.png)

### 2. Navegação básica
Em seguida, fizemos uma navegação básica pelo terminal:
- Verificamos o diretório atual
```
pwd
```
![imagem de exemplo](imgs/02-img.png)

- Listagem de arquivos
```
ls
```
![imagem de exemplo](imgs/03-img.png)

- Criação de pastas
```
mdkir atividades
```
- Entrar em pastas 
```
cd atividades
```
![imagem de exemplo](imgs/04-img.png)

- Voltar para pastas anteriores
```
cd..
pwd
```
![imagem de exemplo](imgs/05-img.png)


### 3. Manipulação de arquivos
Na etapa seguinte, focamos em fazer a manipulação de arquivos, criar, copiar, mover, e excluir arquivos. Criamos um arquivo.txt, mudamos o nome para: *documento.txt*, fizemos uma cópia para outra pasta, e por fim excluímos o arquivo original.

Em seguida, fizemos uma navegação básica pelo terminal:
- Pasta Home do usuário
```
cd ~
```
![imagem de exemplo](imgs/06-img.png)

- Criando e renomeando um arquivo
```
touch arquivo1.txt
ls
mv arquivo1.txt documento.txt
ls
```
![imagem de exemplo](imgs/07-img.png)
- Entrando no diretório ativividades
```
cd atividades
```
![imagem de exemplo](imgs/08-img.png)
- Criando uma pasta e copiando um arquivo pra ela
```
mkdir backup
cp ~/documento.txt backup/
ls backuo/
```

![imagem de exemplo](imgs/09-img.png)

- Voltando pra home, vendo o caminho e apagando um arquivo

```
cd ~
pwd
rm documento.txt
```
![imagem de exemplo](imgs/10-img.png)



### 4. Gerenciamento de pacotes
Nesta etapa, o foco foi realizar operações de instalação de pacotes. O procedimento foi o seguinte:

1. Atualizamos os pacotes presentes no contâiner

![imagem de exemplo](imgs/11-img.png)

2. Instalamos o editor de texto *nano*

![imagem de exemplo](imgs/12-img.png)

3. Vemos a versão do *nano* instalado

![imagem de exemplo](imgs/13-img.png)

4. Por fim, desinstalamos o *nano*


![imagem de exemplo](imgs/14-img.png)


### 5. Permissões dos arquivos
Neste momento, buscamos compreender como é feito a modificação da permissão dos arquivos. Criamos um arquivo.sh, demos a permissão de execução usando *chmod u+x script.sh*, e por fim verificamos as permissões. Não pude compreender muito bem em relação a termos de execução, quem possui a execução do arquivo ou não.

![imagem de exemplo](imgs/15-img.png)


### 6. Processos em execução
Nesta etapa, buscamos analisar os processos em execução: 
- Listando os processos
- Executando um processo em segundo plano
- Buscando o PID dos processos
- Encerrando

![imagem de exemplo](imgs/16-img.png)
![imagem de exemplo](imgs/17-img.png)
![imagem de exemplo](imgs/18-img.png)
![imagem de exemplo](imgs/19-img.png)

### 7. Encerrando o contâiner
Por fim, finalizamos a atividade saindo, e fechando o contâiner.

![alt text](image.png)

### Conclusão
Esse exercício me ajudou a praticar comandos essenciais do Linux e também reforçou meu uso do Docker. Por exemplo, eu nunca tinha usado pwd antes, mesmo tendo alguma experiência com terminal.

Também percebi que o terminal é bem prático, mas ao mesmo tempo, exige atenção. Por exemplo, quando você remove um arquivo com rm, não aparece nenhuma confirmação — só dá pra ver se funcionou com ls.
