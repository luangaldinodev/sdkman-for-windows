# SDKMAN para Windows
Esta documentação orienta a instalação do SDKMAN! no Windows via WSL (Windows Subsystem for Linux), além da configuração do Java, Maven e Quarkus.

## 1. Instalação do linux via terminal

1. Abra o CMD ou PowerShell como administrador e execute o seguinte comando:

``` 
wsl --install
```

2. O Windows baixará e instalará automaticamente o WSL com a distribuição Ubuntu como padrão.

3. Após a instalação, reinicie o computador.

4. Após a reinicialização, abra o CMD ou PowerShell como administrador e execute:

```
wsl -d Ubuntu
```
Isso garantirá que o Ubuntu seja iniciado corretamente dentro do WSL.

## 2. Instalação de pacotes essenciais 
Atualize os pacotes do sistema e instale unzip e zip:

```
sudo apt update && sudo apt install unzip -y
```

```
sudo apt update && sudo apt install zip -y
```

## 3. Instalação do SDKMAN
O SDKMAN! é um gerenciador de versões para Java e outras ferramentas de desenvolvimento. Para instalá-lo, execute:

```
curl -s "https://get.sdkman.io" | bash
```
Após a instalação, carregue o SDKMAN! no terminal:

```
source "$HOME/.sdkman/bin/sdkman-init.sh"
```
Verifique se a instalação foi bem-sucedida:
```
sdk version
```

## 4. Instalação do Java via SDKMAN!
1. Liste as versões disponíveis do Java:
```
sdk list java
```
2. Instale a versão desejada (por exemplo, Java 17 da Amazon):
```
sdk install java <versão>
```
**Exemplo:**
```
sdk install java 17-amzn
```
3. Verifique a instalação do Java:
```
java -version
```

## 5. Instalação do Maven e Quarkus
Instale o Maven e o Quarkus utilizando o SDKMAN!:
```
sdk install maven
```

```
sdk install quarkus
```

## 6. Instalação do navegador Firefox


```
sudo apt install firefox -y
```

Para executar o navegador, volte ao Windows, procure por **Firefox (Ubuntu)** e execute-o como administrador.


## 7. Criando um projeto Quarkus
1. Crie um novo projeto Quarkus:
```
quarkus create app hello-world
```
2. Acesse o diretório do projeto:
```
cd hello-world
```
3. Inicie o servidor de desenvolvimento:
```
quarkus dev
```
4. Acesse a aplicação via localhost, conforme indicado no terminal do WSL.

**ATENÇÃO:** Verifique a porta na qual a aplicação está rodando.

### Informações de Contato

Caso precise de mais assistência, entre em contato comigo:

* Email: luangaldinodev@gmail.com
* Telefone: (12) 98282-7309