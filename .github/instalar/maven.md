<h1>
    <a href="https://github.com/elizabetefabri">
     <img align="center" width="40px" src="../../.github/JAVA.png"></a>
    <span>Maven</span>
</h1>

## 1. Maven no Windows
- [Baixar o arquivo do Maven](https://dlcdn.apache.org/maven/maven-3/3.9.5/binaries/apache-maven-3.9.5-bin.zip)

## 2. Descompactar o arquivo baixado. 

**Atenção: No momento de descompactar o arquivo, é importante colocar em um local de fácil acesso. Uma dica é descompactar no C: , e renomear  a pasta para maven**

## 3. Após descompactar, acessar as variáveis de ambiente, clicando em **Este Compuador > Propriedades**
![App Screenshot](./img/img-11.png)

## 4. Clicar em Configurações avançadas do sistema
![App Screenshot](./img/img-12.png)

### 5. Na aba avançado clicar em Variáveis de ambiente
![App Screenshot](./img/img-13.png)

### 6. Selecione a variável Path e clique em Editar
![App Screenshot](./img/img-14.png)

### 7. Clique no botão novo e adicione o caminho da pasta bin do maven: C:\maven\bin  e clique em ok
![App Screenshot](./img/img-15.png)

### 8. Acesse o terminal e digite o comando mvn . O resultado esperado deverá ser o seguinte
![App Screenshot](./img/img-16.png)

## Maven no Linux

1-  Atualize os pacotes

`sudo apt-get update`

2 - Instale o maven com o seguinte comando

`sudo apt-get -y install maven`

O maven deverá ser instalado em um dos seguintes caminhos **/usr/share/maven**
 ou **/etc/maven**
.

Para verificar se o maven foi instalado com sucesso, acessar o terminar e digitar

`mvn -version`

Isso irá mostrar a versão do maven instalada.