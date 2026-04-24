<div align="center">

<img src="https://raw.githubusercontent.com/Shadoww111/smartpark/main/docker/imgs/SmartPark-removebg-preview.png" alt="SmartPark Logo" width="180"/>

# SmartPark

**Plataforma SaaS de Gestão Inteligente de Estacionamento**

[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white)](https://docker.com)
[![Stripe](https://img.shields.io/badge/Stripe-Connect-635BFF?style=flat-square&logo=stripe&logoColor=white)](https://stripe.com)
[![MariaDB](https://img.shields.io/badge/MariaDB-10.6+-003545?style=flat-square&logo=mariadb&logoColor=white)](https://mariadb.org)

*Projeto de Aptidão Profissional — Escola Profissional Ruiz Costa · TGPSI 2023/2026*

[🌐 Landing Page](https://landingpage-sp.ruicosta.pt) · [📊 Dashboard](https://dashboard-sp.ruicosta.pt) · [📱 PWA Condutor](https://pay-sp.ruicosta.pt/?park=7)

</div>

---

## O que é o SmartPark?

O SmartPark elimina máquinas físicas, tickets em papel e quiosques de pagamento nos parques de estacionamento. O sistema une três componentes num único produto:

- **A matrícula é o bilhete** — câmara lê a matrícula na entrada e na saída, sem interação física
- **O telemóvel é o pagamento** — condutor paga via PWA com QR Code, com 6 métodos Stripe
- **A cancela abre sozinha** — Arduino recebe o sinal e aciona a cancela automaticamente

Oferecido como **SaaS** — o operador subscreve um plano, ativa a licença, e tem o parque operacional em minutos.

---

## Experimente

<div align="center">

| | |
|:---:|:---:|
| [**🌐 Landing Page**](https://landingpage-sp.ruicosta.pt) | Página de produto com planos e funcionalidades |
| [**📊 Dashboard**](https://dashboard-sp.ruicosta.pt) | Painel de gestão do operador |
| [**📱 PWA do Condutor**](https://pay-sp.ruicosta.pt/?park=7) | Pagamento self-service — Stripe em modo de teste |

</div>

---

## Funcionalidades

### Para o condutor
- Acesso via QR Code sem instalar nada
- **6 métodos de pagamento** — Cartão, MB Way, Multibanco, Apple Pay, Google Pay, Revolut Pay
- Recibo digital com opção de partilha
- Sem filas, sem máquinas, sem dinheiro físico

### Para o operador
- Dashboard em tempo real com atualização automática
- Tarifação dinâmica por hora e dia da semana
- Controlo de acessos por funções (Owner, Admin, Operator)
- Histórico e exportação de dados
- Stripe Connect — pagamentos diretos para a conta do operador

### Para a plataforma
- Subscrições com 3 planos (Mensal, Semestral, Anual)
- Sistema de licenciamento com grace period e alertas automáticos
- Suporte a múltiplos parques por conta

---

## Stack Tecnológico

<div align="center">

| Camada | Tecnologias |
|---|---|
| **Frontend** | React 18 · TypeScript · TailwindCSS · shadcn/ui |
| **Backend** | Node.js · Express · JWT · Stripe SDK |
| **ALPR** | Python · FastAPI · OpenCV · EasyOCR |
| **Base de dados** | MariaDB |
| **Infraestrutura** | Docker Compose · Nginx |
| **Hardware** | Arduino Uno · Câmara USB · Servo Motor |

</div>

---

## Em Números

<div align="center">

| **3** | **6** | **3** |
|:---:|:---:|:---:|
| Serviços backend independentes | Contentores Docker | Apps React |
| **6** | **< 1s** | **90 €** |
| Métodos de pagamento Stripe | Latência SSE no dashboard | Custo total de hardware |

</div>

---

## Hardware da Maquete

Maquete física funcional construída com componentes acessíveis para demonstração em ambiente real.

| Componente | Custo |
|---|---|
| Kit Arduino Uno | 40 € |
| Câmara Logitech USB | 35 € |
| USB-C Hub | 15 € |
| **Total** | **90 €** |

---

## ODS Associados

- **ODS 9 — Inovação:** Tecnologia de gestão de estacionamento acessível a qualquer operador
- **ODS 11 — Cidades Sustentáveis:** Menos tempo à procura de lugar, sem dependência de hardware físico
- **ODS 17 — Parcerias:** Stripe Connect liga operadores independentes à plataforma diretamente

---

<div align="center">

**Pedro Miguel Gonçalves Costa**

Técnico de Gestão e Programação de Sistemas Informáticos
Escola Profissional Ruiz Costa · 2023/2026

[GitHub](https://github.com/Shadoww111) · [Landing Page](https://landingpage-sp.ruicosta.pt) · [Demo](https://pay-sp.ruicosta.pt/?park=7)

</div>
