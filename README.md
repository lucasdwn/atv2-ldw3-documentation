# List-tasks: Gerenciador de Tarefas

[![TypeScript](https://img.shields.io/badge/TypeScript-4.x-blue)](https://www.typescriptlang.org/) 
[![MongoDB](https://img.shields.io/badge/MongoDB-5.x-green)](https://www.mongodb.com/) 
[![Node.js](https://img.shields.io/badge/Node.js-18.x-green)](https://nodejs.org/) 
[![Express](https://img.shields.io/badge/Express-4.x-black)](https://expressjs.com/) 
[![Next.js](https://img.shields.io/badge/Next.js-13.x-black)](https://nextjs.org/) 
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.x-blue)](https://tailwindcss.com/)
[![Shadcn-UI](https://img.shields.io/badge/Shadcn--UI-Components-orange)](https://ui.shadcn.dev/)
[![JWT](https://img.shields.io/badge/JSONWebTokens-8.x-yellow)](https://www.npmjs.com/package/jsonwebtoken)
[![Bcrypt](https://img.shields.io/badge/Bcrypt-5.x-yellowgreen)](https://www.npmjs.com/package/bcrypt)
[![AWS-S3](https://img.shields.io/badge/AWS--S3-Cloud-orange)](https://aws.amazon.com/s3/)

## Apresentação
Este projeto é um Gerenciador de Tarefas que implementa um sistema CRUD (Create, Read, Update, Delete) completo. Ele foi desenvolvido utilizando TypeScript para garantir maior segurança e escalabilidade do código, juntamente com MongoDB como banco de dados para armazenar as informações de usuários, listas e tarefas.

Com esta aplicação, os usuários podem gerenciar suas atividades diárias, organizar listas de tarefas, definir prioridades, criar subtarefas, anexar arquivos e compartilhar listas com outros usuários. O objetivo principal é fornecer uma ferramenta intuitiva para ajudar no planejamento e execução de tarefas, seja para projetos pessoais ou profissionais.

### Apresentação em Vídeo
[Assista Aqui](https://youtu.be/pxnRsuvfBCc)
### Teste a aplicação
[Acesse Aqui](https://atv2-ldw3-front.vercel.app)


## Enunciado

**Atividade:**  
Atividade 2 da matéria **Laboratório de Desenvolvimento WEB 3**: Implementação de um sistema CRUD (Create, Read, Update, Delete) para um Gerenciador de Tarefas com TypeScript e MongoDB.

**Objetivo:**  
Desenvolver uma aplicação completa em TypeScript que permita a criação, leitura, atualização e exclusão de registros de um Gerenciador de Tarefas (como se fosse uma agenda) em um banco de dados MongoDB, garantindo a persistência e integridade dos dados.

### Funcionalidades Essenciais:

#### Listas
- **Tipos de listas:** Tarefas, projetos, compras, etc.
- **Personalização:** Nomes de listas, cores, ícones.

#### Tarefas
- **Atributos:** Título, descrição, data de vencimento, prioridade, status (pendente, concluída, atrasada).
- **Subtarefas:** Divisão de tarefas maiores em partes menores.
- **Anexos:** Possibilidade de adicionar arquivos (documentos, imagens) às tarefas.

#### Prioridades
- **Níveis de prioridade:** Alta, média, baixa.
- **Personalização:** Possibilidade de criar níveis de prioridade personalizados.

#### Prazos
- **Data e hora:** Definição precisa do prazo.
- **Alertas:** Notificações antes do prazo.

#### Busca e Filtragem
- **Busca por palavras-chave:** Título, descrição, listas.
- **Filtros:** Por data, prioridade, status, lista.

#### Compartilhamento
- **Compartilhamento de listas:** Possibilidade de compartilhar listas com outros usuários.

## Tecnologias Utilizadas

- **TypeScript**: Tipagem estática e robustez.
- **Node.js**: Execução do código em JavaScript no lado do servidor.
- **Express.js**: Framework para criação de APIs RESTful.
- **MongoDB**: Banco de dados NoSQL para armazenamento de informações.
- **Bcrypt**: Criptografia de senhas.
- **AWS S3**: Armazenamento de arquivos.
- **JWT (JsonWebToken)**: Autenticação com tokens.
- **Next.js**: Framework para aplicações React no front-end.
- **TailwindCSS**: Framework para estilização com classes utilitárias.
- **Shadcn-UI**: Componentes para interface do usuário.
  
## Estrutura AWS

A aplicação utiliza a **Amazon Web Services (AWS)** para armazenar e distribuir arquivos. A estrutura de armazenamento e distribuição foi implementada da seguinte forma:

- **S3 Bucket Privado**: Todos os arquivos enviados pelos usuários (como anexos em tarefas) são armazenados em um bucket privado do S3, o que garante que esses arquivos não tenham acesso público direto.
- **CloudFront**: Para distribuir esses arquivos na internet de forma segura, o **CloudFront** (um serviço de CDN) é utilizado. Isso permite que os arquivos sejam acessados pelos usuários através de uma URL temporária e protegida, sem a necessidade de expor o bucket S3 publicamente. Essa estrutura garante maior segurança e controle sobre os dados armazenados.

## Modelo de Dados no MongoDB

Abaixo está a representação do modelo de dados utilizado no MongoDB:

![Modelo de Dados](./models.png)

## Wireframes

Aqui estão os wireframes que foram usados como referência para o desenvolvimento da aplicação:

![Wireframes](./Wireframes.png)

## Como Rodar o Projeto

Este projeto é dividido em duas partes: a API e o front-end. Siga as instruções dos respectivos repositórios para configurar e rodar cada parte.

### 1. Rodar a API

Para configurar e rodar a API do projeto, siga as instruções descritas no repositório da API:

[Repositório da API - Instruções de Execução](https://github.com/lucasdwn/atv2-ldw3-api)

#### Opção de Uso Rápido para a API

Caso você não queira configurar a AWS para o armazenamento de arquivos, você pode utilizar o release **'Upload-Local'**, que já vem configurado para armazenar os arquivos localmente. Para isso, siga os passos abaixo:

1. **Baixe o Release 'Upload-Local':**
   - Acesse a seção de releases do repositório da API.
   - Baixe o arquivo correspondente ao release **'Upload-Local'**.

2. **Extraia e Execute:**
   - Extraia o arquivo em uma pasta de sua escolha.
   - Navegue até essa pasta pelo terminal.
   - Configure as váriaveis de ambiente em `.env`.
   - Execute o comando:
     ```bash
     npm install
     npm start
     ```

### 2. Rodar o Front-End

Para configurar e rodar o front-end do projeto, siga as instruções descritas no repositório do front-end:

[Repositório do Front-End - Instruções de Execução](https://github.com/lucasdwn/atv2-ldw3-front)

#### Opção de Uso Rápido para o Front-End

Assim como na API, caso você não queira configurar a AWS, pode usar o release **'Upload-Local'** disponível para o front-end. Para isso:

1. **Baixe o Release 'Upload-Local':**
   - Acesse a seção de releases do repositório do front-end.
   - Baixe o arquivo correspondente ao release **'Upload-Local'**.

2. **Extraia e Execute:**
   - Extraia o arquivo em uma pasta de sua escolha.
   - Navegue até essa pasta pelo terminal.
   - Configure as váriaveis de ambiente em `.env`.
   - Execute o comando:
     ```bash
     npm install
     npm start
     ```

3. **Acesse a Aplicação:**
   - Após a execução, abra seu navegador e acesse `http://localhost:3000`.

Com essas configurações, você poderá testar a aplicação rapidamente em ambas as partes, sem a necessidade de configurações complexas de armazenamento em nuvem.