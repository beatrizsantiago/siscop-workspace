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

📍 Para iniciar todos os serviços com Docker:

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
