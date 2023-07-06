# teste-java-r2
Teste de nivel para desenvolvedores Convergência

# Objetivo

O objetivo deste teste é avaliar o conhecimento técnico do candidato em relação a arquitetura de software, boas práticas de programação, conhecimento em banco de dados e conhecimento em frameworks Java.

# Descrição

O candidato deverá desenvolver duas aplicações Java, uma para gerir CPFs (ativos e inativos) e outra para gerir Logins.
As aplicações deverão ser desenvolvidas utilizando o framework Spring Boot e banco de dados H2.

Por favor utilize o template abaixo para desenvolver as aplicações:
https://start.spring.io/#!type=maven-project&language=java&platformVersion=2.7.3&packaging=jar&jvmVersion=18&groupId=br.com.convergencia&artifactId=teste-java-r2&name=teste-java-r2&description=Teste%20de%20nivel%20para%20desenvolvedores%20Convergencia&packageName=br.com.convergencia.teste-java-r2&dependencies=web,data-jpa,h2

# Requisitos

## CPF

- Deverá ser possível cadastrar um CPF;
- Deverá ser possível consultar o status de um CPF;
- Um CPF inativo não poderá ser reativado;
- Após 7 dias sem login, o CPF deverá ser marcado como inativo;
- Um CPF inativo não poderá ser utilizado para realizar login;

## Login

- Deverá ser possível cadastrar um login;
- Deverá ser possível realizar o login;
- O login deverá ser realizado utilizando o CPF cadastrado e ativo;
- Em caso de 3 tentativas de login com CPF inativo, o login deverá ser bloqueado por 24 horas;
- Em caso de 3 tentativas de login com CPF ativo, o login deverá ser bloqueado por 1 hora;
- Após o prazo de bloqueio, um e-mail deverá ser enviado para o usuário informando que o login foi desbloqueado;

# Arquitetura

![Arquitetura](/arquitetura.png "Documento de Arquitetura do Sistema")

Iremos utilizar a arquitetura de microsserviços, onde cada serviço será responsável por uma funcionalidade do sistema. A comunicação entre os serviços será feita utilizando o protocolo HTTP e o formato JSON.

# Testes

 - Ambos os serviços deverão possuir testes unitários;
 - Ambos os serviços deverão ser entregues com um arquivo Dockerfile para que possamos subir os serviços em um container Docker;
 - Ambos os serviços devem possuir um arquivo Postman Collection para que possamos testar as funcionalidades.

# Dúvidas

O teste tem um escopo bem definido mas existe espaço para interpretação. Em caso de dúvidas, por favor anote a dúvida e envie junto com o teste. Não iremos responder dúvidas durante o desenvolvimento do teste, pois queremos avaliar a capacidade de interpretação do candidato.

# Critérios de avaliação

 - Código funcional;
 - Requisitos atendidos;
 - Práticas de mercado na construção do código;
 - Aderência aos padrões de API REST;
 - Código limpo;

# Entrega

O candidato deverá desenvolver o teste em um repositório privado no GitHub e dar acessso ao usuário @convergencia para que possamos avaliar o código.
Crie um arquivo `Business.md` na raiz do repositório com as decisões de negócio tomadas durante o desenvolvimento do teste.
Pedimos que o candidato não faça o fork do repositório para não tornar a sua solução pública.