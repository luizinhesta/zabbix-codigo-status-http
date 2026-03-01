# 📊 Zabbix - Monitoramento HTTP Status Code

![HTTP Status Code](Imagens/imagem(1).jpg)

Este projeto demonstra como monitorar aplicações web utilizando **Zabbix
Web Scenarios**, destacando a diferença entre:

-   Monitoramento de rede (ICMP Ping)
-   Monitoramento de aplicação via **HTTP Status Code**
-   Validação de login em aplicações web (WordPress)
-   Criação de Trigger para alertar quando a página deixa de retornar
    HTTP 200

------------------------------------------------------------------------

## 🎯 Objetivo

Demonstrar na prática que:

> **Ping ≠ Aplicação funcionando**

Um servidor pode responder na rede enquanto a aplicação retorna erro
HTTP.

------------------------------------------------------------------------

## 🌐 Códigos de Status HTTP

A imagem abaixo foi utilizada como apoio didático durante a
demonstração.

![HTTP Status Code](imagens/imagem(2).jpg)

### Classificação

  Código   Significado
  -------- ------------------
  1xx      Informacional
  2xx      Sucesso
  3xx      Redirecionamento
  4xx      Erro do Cliente
  5xx      Erro do Servidor

------------------------------------------------------------------------

## 🛰️ Monitoramento ICMP (Ping)

Template utilizado:

    Template Module ICMP Ping

Valida apenas conectividade de rede.

------------------------------------------------------------------------

## 🌍 Web Scenario - Status HTTP 200

Configuração realizada:

-   URL monitorada
-   Follow redirects habilitado
-   Required status code: **200**

------------------------------------------------------------------------

## 🔐 Monitoramento de Login WordPress

Fluxo configurado:

1.  Acesso ao wp-login.php
2.  Envio do formulário de autenticação
3.  Validação do painel administrativo

Macros utilizadas:

    {$WP.USER}
    {$WP.PASS}

------------------------------------------------------------------------

## 🚨 Trigger criada

Trigger utilizada para detectar falha quando a página não retorna HTTP
200:

``` zabbix
last(/wordpress-ct/web.test.rspcode[WP - Site status,Site])<>200
```

------------------------------------------------------------------------

## 🖼️ Galeria de Imagens do Projeto

> Nesta seção serão adicionadas **6 imagens**, organizadas em **2 linhas
> e 3 colunas**.

|  |  |  |
|------|-------------|---------|
| ![](imagens/imagem(1).png) | ![](imagens/imagem(2).png) | ![](imagens/imagem(3).png) |
| ![](imagens/imagem(4).png) | ![](imagens/imagem(5).png) | ![](imagens/imagem(6).png) |
| ![](imagens/imagem(7).png) | ![](imagens/imagem(8).png) | ![](images/imagem(00).png) |

------------------------------------------------------------------------

## 🛠️ Tecnologias Utilizadas

-   Zabbix
-   WordPress
-   HTTP Protocol
-   ICMP
-   Web Monitoring

------------------------------------------------------------------------

## 🎥 Video Aula

Este repositório acompanha videoaula demonstrando:

-   Monitoramento por Ping
-   Monitoramento HTTP Status Code
-   Diferença entre rede e aplicação
-   Validação de login real

------------------------------------------------------------------------

## 🌐 Minhas redes

- 📺 **YouTube:** `https://youtu.be/uBxlQj4nvjg` 
- 💼 **LinkedIn:** `https://www.linkedin.com/in/luiz-inhesta-341b4b311/` 

---

## 👨‍💻 Autor

Luiz Augusto\
Infrastructure • Cloud • Monitoring 🚀
