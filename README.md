# Siscop Workspace

**Repositório principal do projeto desenvolvido durante o Hackathon da Pós-Tech FIAP.**

## ✨ Sobre o Projeto

Este workspace reúne todos os projetos que compõem o **Siscop**, uma solução voltada para a gestão e o acompanhamento de processos agrícolas.  

---

## 🧩 Microfrontend

O sistema web foi desenvolvido com base na arquitetura de **microfrontends**, garantindo uma separação clara de responsabilidades entre os módulos.

- [`siscop-root`](https://github.com/beatrizsantiago/siscop-root) — Módulo principal que orquestra a composição dos microfrontends.
- [`siscop-products`](https://github.com/beatrizsantiago/siscop-products) — Gerenciamento de produtos agrícolas.
- [`siscop-farms`](https://github.com/beatrizsantiago/siscop-farms) — Administração de fazendas e suas informações.
- [`siscop-inventory`](https://github.com/beatrizsantiago/siscop-inventory) — Controle de estoque de insumos e produtos.
- [`siscop-goals`](https://github.com/beatrizsantiago/siscop-goals) — Definição e acompanhamento de metas produtivas.
- [`siscop-sales`](https://github.com/beatrizsantiago/siscop-sales) — Gestão de vendas e transações.
- [`siscop-production`](https://github.com/beatrizsantiago/siscop-production) — Monitoramento e análise de dados de produção.

> 📍 A partir da **pasta raiz do workspace**, siga as instruções abaixo para executar o microfrontend com Docker:

### 🔧 Configurações do Firebase

1. **Criar conta**

  - Crie uma conta ou [acesse o console](https://console.firebase.google.com/) do Firebase usando sua conta Google.

2. **Criar um novo projeto**

  - Siga este [guia oficial](https://firebase.google.com/docs/web/setup) para criar um novo projeto.
  - Após criar o projeto, acesse a aba Configurações do Projeto (ícone de engrenagem no menu lateral).
  - Na seção Suas Apps, clique em "Web" para registrar uma nova aplicação Web.
  - Ao finalizar o registro, o Firebase irá exibir o seu Firebase Config — um objeto contendo informações como apiKey, projectId, storageBucket, entre outros.

3. **Configurar variáveis de ambiente**

> Um arquivo de exemplo chamado ```.env.example``` está disponível no projeto. Use-o como base para criar o seu arquivo de configuração:

  ```bash
  cp .env.example .env
  ```

  3.1. Crie um arquivo chamado `.env` na raiz do workspace.

  3.2. Copie e preencha a estrutura abaixo com os dados fornecidos pelo Firebase:

  ```js
  // .env

  VITE_FIREBASE_API_KEY={{ API_KEY }}
  VITE_FIREBASE_AUTH_DOMAIN={{ DOMINIO.firebaseapp.com }}
  VITE_FIREBASE_PROJECT_ID={{ PROJECT_ID }}
  VITE_FIREBASE_STORAGE_BUCKET={{ BUCKET.appspot.com }}
  VITE_FIREBASE_MESSAGING_SENDER_ID={{ SENDER_ID }}
  VITE_FIREBASE_APP_ID={{ APP_ID }}
  ```

4. **Habilitar Autenticação e Firestore**

  No console do Firebase, acesse:

  - [Autenticação](https://firebase.google.com/docs/auth/web/email-link-auth): Habilite o método de email/senha e o login com o google para autenticação.
  - [Firestore](https://firebase.google.com/docs/firestore/quickstart): Crie um banco de dados Firestore.

5. **Configurar regras do Firestore**

  No Firestore, adicione as [regras de acesso](https://firebase.google.com/docs/firestore/security/get-started) abaixo (configuração disponível na aba de "Regras"):

  ```bash
    rules_version = '2';
    service cloud.firestore {
      match /databases/{database}/documents {
        match /{document=**} {
          allow read, write: if true;
        }
      }
    }
  ```

### 🔧 Configurações do Google Maps

> Para utilizar o Google Maps no projeto é necessário configurar uma chave de API na plataforma da Google Cloud.

1. **Acesse o Console do Google Cloud:**

   [https://console.cloud.google.com/](https://console.cloud.google.com/)

2. **Crie um novo projeto** (ou selecione um existente).

3. No menu lateral, vá em **"APIs e serviços"**.

4. **Habilite as seguintes APIs:**

   - Maps JavaScript API
   - Maps SDK for Android
   - Maps SDK for iOS

5. Vá para **"Chaves e credenciais"** e clique em **"Criar credenciais" > "Chave de API"**.

6. No arquivo `.env` adicione a chave api do google maps, como no exemplo abaixo:

```js
// .env
VITE_JAVASCRIPT_MAPS_API={{ MAPS_API_KEY }}
```

### ▶️ Executando com Docker

> 💡 Certifique-se de estar na **pasta raiz do workspace** e de ter o **Docker instalado** antes de executar o comando abaixo:

```bash
docker-compose up --build
```

> 🛠️ Para utilizar o projeto **sem Docker**, é necessário acessar cada pasta individualmente e seguir as instruções específicas de configuração.  
> Cada projeto possui instruções no seu respectivo **README**, incluindo detalhes sobre a configuração do ambiente.

---

## 🎨 Design System

- [`agro-core`](https://github.com/beatrizsantiago/agro-core) — Design system utilizado para unificar a identidade visual e componentes compartilháveis do ecossistema.

> 📍 Acesse a pasta do `agro-core`, instale as dependências e siga as instruções do **README** para visualizar a documentação corretamente.

---

## 📱 Mobile

- [`siscop-mobile`](https://github.com/beatrizsantiago/siscop-mobile) — Aplicativo móvel desenvolvido com React Native, focado em acessibilidade e uso em campo.

>📍 Acesse a pasta do `siscop-mobile`, instale as dependências e siga as instruções do **README** para configurar o ambiente corretamente.
