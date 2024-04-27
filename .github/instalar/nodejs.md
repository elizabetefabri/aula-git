<h1>
    <a href="https://github.com/elizabetefabri">
     <img align="center" width="40px" src="../../.github/JAVA.png"></a>
    <span>Node e NPM</span>
</h1>

## 1. O primeiro passo é instalar o Node.js, que vem acompanhado do NPM.

### 1.1 Windows
Para o Windows utilizaremos o gerenciador de pacotes [Chocolatey,](https://chocolatey.org/) porém antes dos passos de instalação vamos falar brevemente sobre qual shell você deve usar.

- **CMD**: também conhecido como **Command Prompt**, ele é um dos shells mais antigos da atualidade (foi construído para ser compatível com o **MS-DOS**) e, apesar da sua fama, hoje em dia tem sido cada vez menos utilizado.
- **Powershell**: novo shell apresentado pela Microsoft por volta de 2005, ele apresenta diversas melhorias em relação ao **CMD**, tornando-o popular atualmente.

Escolhido o shell, vamos começar a instalação:

- Busque no campo de busca do Windows por **Windows Powershell**, clique com o botão direito em cima do programa e escolha a opção **Executar como administrador**.
- O Powershell trabalha com um esquema de autorizações (conhecido como `Execution Policy`) para execução de scripts e, por isso, precisamos verificar se o presente no sistema está compatível com o que o Chocolatey precisa. Execute o seguinte comando:

```bash
Get-ExecutionPolicy
```

Caso ele retorne `Restricted`, execute o comando:

```bash
Set-ExecutionPolicy RemoteSigned
```

E escolha a opção `[A] Sim para Todos`

```
⚠️ Caso o comando acima apresente erro, tente usar:

    Set-ExecutionPolicy Bypass -Scope Process
```
Verifique se alteração de permissão ocorreu com sucesso executando novamente o comando:

```
Get-ExecutionPolicy
```
​
Alterada a permissão, basta instalar o Chocolatey com o comando:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
​
```
Caso o comando acima apresente um erro, verifique se a sua máquina atende às requisições mínimas

Windows 7+ / Windows Server 2003+
PowerShell v3+
.NET Framework 4.5+
Caso o erro apresentado seja Exceção ao definir "SecurityProtocol": "Não é possível converter o valor "3312", 
siga esse: [guia](https://blog.chocolatey.org/2020/01/remove-support-for-old-tls-versions/).

``` 

- Após o fim da instalação, feche e abra o powershell como administrador novamente e execute:

```
choco -v
```

Caso ele retorne a versão do **Chocolatey**, a instalação foi um sucesso. Para finalizar, basta instalar a versão LTS mais recente do Node com o seguinte comando:

```bash
cinst nodejs-lts
```

E escolha a opção `[A]ll - yes to all`

Após o fim da instalação, feche e abra o powershell como administrador novamente e execute:

```bash
node -v
npm -v
```

Caso retorne as versões do Node e npm, sua instalação foi um sucesso.

## Windows - YARN

Para instalar o Yarn 1 no Windows siga os seguintes passos, execute o comando no Powershell (como admin):

```bash
 cinst yarn
```

E escolha a opção `[A]ll - yes to all`. 

Feche e abra o terminal novamente, em seguida rode o comando:

```bash
 yarn --version
```

Caso retorne a versão do Yarn (acima de 1.0, abaixo de 2.0), a instalação ocorreu com sucesso.

### Possíveis problemas
Ao usar o Yarn no Windows para instalar as dependências nos seus projetos, atente-se para que seu nome de usuário não possua espaços, pois nesse caso, alguns erros poderão ocorrer durante esse processo, como por exemplo: com o nome "elizabete", o caminho até a pasta do projeto (supondo que estivesse na pasta *Documents*) seria algo como `C:\Users\elizabete\Documents\www\Projeto` e nesse caso, uma solução seria criar o projeto já na raiz do **Disco C**. Dessa forma, o caminho até a pasta não passaria pelo nome do usuário, ficando `C:\www\Projeto`.

