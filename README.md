<div align="center">

# SmartPark

### Plataforma SaaS de Gestão Inteligente de Estacionamento

*A matrícula é o bilhete. O telemóvel é o pagamento. A cancela abre sozinha.*

<br/>

[![Node.js](https://img.shields.io/badge/Node.js-18-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com)
[![Stripe](https://img.shields.io/badge/Stripe-Connect-635BFF?style=for-the-badge&logo=stripe&logoColor=white)](https://stripe.com)
[![MariaDB](https://img.shields.io/badge/MariaDB-10.6-003545?style=for-the-badge&logo=mariadb&logoColor=white)](https://mariadb.org)

<br/>

**[Landing Page](https://landingpage-sp.ruicosta.pt)** &nbsp;&nbsp;·&nbsp;&nbsp; **[Dashboard](https://dashboard-sp.ruicosta.pt)** &nbsp;&nbsp;·&nbsp;&nbsp; **[PWA do Condutor](https://pay-sp.ruicosta.pt/?park=7)**

</div>

<br/>

---

<br/>

## O problema

Os parques de estacionamento pequenos e médios continuam a operar com hardware físico obsoleto: máquinas de tickets, quiosques de pagamento, cancelas manuais. As plataformas profissionais que resolvem isto — Designa, SABA, Indigo — são sistemas fechados e proprietários, inacessíveis a operadores independentes.

O resultado: o condutor é forçado a interagir com máquinas, o operador não tem visibilidade em tempo real sobre o seu próprio parque, e a tecnologia moderna não chega a quem mais precisa dela.

## A solução

O SmartPark é uma plataforma completa que resolve o problema ponta a ponta. Uma câmara reconhece a matrícula do veículo na entrada — é o bilhete. O condutor paga pelo telemóvel através de um QR Code — é o pagamento. Um Arduino aciona a cancela automaticamente — a saída é instantânea.

Tudo isto é oferecido como **Software as a Service**. O operador subscreve um plano, ativa a licença, liga o hardware e tem o parque operacional em minutos.

<br/>

---

<br/>

## Produto ao vivo

<table width="100%">
<tr>
<td width="33%" align="center">
<h3>Landing Page</h3>
<a href="https://landingpage-sp.ruicosta.pt">landingpage-sp.ruicosta.pt</a>
<br/><br/>
<sub>Página de produto com planos,<br/>funcionalidades e subscrição</sub>
</td>
<td width="33%" align="center">
<h3>Dashboard</h3>
<a href="https://dashboard-sp.ruicosta.pt">dashboard-sp.ruicosta.pt</a>
<br/><br/>
<sub>Painel de gestão multi-parque<br/>em tempo real para o operador</sub>
</td>
<td width="33%" align="center">
<h3>PWA do Condutor</h3>
<a href="https://pay-sp.ruicosta.pt/?park=7">pay-sp.ruicosta.pt</a>
<br/><br/>
<sub>Pagamento self-service<br/>via QR Code sem instalação</sub>
</td>
</tr>
</table>

> O ambiente de produção corre com Stripe em modo de teste. Cartões aceites para demonstração: `4242 4242 4242 4242` com qualquer CVC e data futura.

<br/>

---

<br/>

## Como funciona

<table>
<tr>
<td width="50%" valign="top">

### Entrada do veículo

A câmara USB captura a matrícula e envia para o serviço ALPR. O backend valida a licença do parque, regista a entrada, e envia um sinal ao Arduino que levanta a cancela.

O dashboard atualiza automaticamente via Server-Sent Events em menos de um segundo.

</td>
<td width="50%" valign="top">

### Saída e pagamento

O condutor lê o QR Code com o telemóvel. A PWA abre com o valor a pagar, calculado dinamicamente com base no tempo de permanência e nas tarifas configuradas pelo operador.

Seis métodos de pagamento disponíveis. Após confirmação, a cancela de saída abre automaticamente.

</td>
</tr>
</table>

<br/>

---

<br/>

## Funcionalidades

### Para o condutor

| | |
|---|---|
| **Sem aplicações** | Acesso via QR Code, funciona em qualquer telemóvel com browser |
| **Seis métodos de pagamento** | Cartão, MB Way, Multibanco, Apple Pay, Google Pay, Revolut Pay |
| **Recibo digital** | Comprovativo guardado no telemóvel com opção de partilha |
| **Sem dinheiro físico** | Nunca mais à procura de moedas ou notas |

### Para o operador

| | |
|---|---|
| **Dashboard em tempo real** | Ocupação, receita e veículos ativos com atualização automática |
| **Tarifação dinâmica** | Regras configuráveis por faixa horária e dia da semana |
| **Controlo de acessos** | Três funções distintas com permissões granulares |
| **Stripe Connect** | Pagamentos transferidos diretamente para a conta bancária do operador |
| **Exportação de dados** | Histórico em CSV, PDF ou JSON a partir de qualquer filtro |

### Para a plataforma

| | |
|---|---|
| **Três planos de subscrição** | Mensal, Semestral e Anual com preços escalonados |
| **Grace period** | Período de graça configurável após expiração com alertas por email |
| **Mudança de plano** | Crédito proporcional aplicado automaticamente ao tempo restante |
| **Multi-parque** | Um operador pode gerir vários parques numa única conta |

<br/>

---

<br/>

## Stack

<table>
<tr>
<td valign="top" width="25%">

**Frontend**
- React 18
- TypeScript
- Vite
- TailwindCSS
- shadcn/ui

</td>
<td valign="top" width="25%">

**Backend**
- Node.js 18
- Express
- MySQL2
- JWT
- Stripe SDK

</td>
<td valign="top" width="25%">

**ALPR**
- Python 3.10
- FastAPI
- OpenCV
- EasyOCR

</td>
<td valign="top" width="25%">

**Infraestrutura**
- Docker Compose
- Nginx
- MariaDB
- Arduino Uno

</td>
</tr>
</table>

<br/>

---

<br/>

## Em números

<table width="100%">
<tr>
<td align="center" width="33%">
<h1>3</h1>
<b>Serviços backend</b>
<br/>
<sub>independentes e escaláveis</sub>
</td>
<td align="center" width="33%">
<h1>6</h1>
<b>Contentores Docker</b>
<br/>
<sub>orquestrados em Compose</sub>
</td>
<td align="center" width="33%">
<h1>6</h1>
<b>Métodos de pagamento</b>
<br/>
<sub>integrados via Stripe</sub>
</td>
</tr>
<tr>
<td align="center" width="33%">
<h1>3</h1>
<b>Aplicações React</b>
<br/>
<sub>Landing, Dashboard, PWA</sub>
</td>
<td align="center" width="33%">
<h1>&lt; 1s</h1>
<b>Latência SSE</b>
<br/>
<sub>no dashboard em tempo real</sub>
</td>
<td align="center" width="33%">
<h1>90€</h1>
<b>Custo de hardware</b>
<br/>
<sub>maquete completa e funcional</sub>
</td>
</tr>
</table>

<br/>

---

<br/>

## Hardware

A maquete física de demonstração foi construída com componentes acessíveis para provar que o sistema funciona em ambiente real.

| Componente | Função | Custo |
|---|---|---:|
| Kit Arduino Uno | Controlo da cancela via porta série | 40 € |
| Câmara Logitech C920 USB | Captura de frames para o ALPR | 35 € |
| USB-C Hub | Gestão de portas de ligação | 15 € |
| | **Total** | **90 €** |

<br/>

---

<br/>

## Objetivos de Desenvolvimento Sustentável

O projeto contribui diretamente para três dos Objetivos de Desenvolvimento Sustentável definidos pela ONU.

**ODS 9 — Indústria, Inovação e Infraestruturas**
Democratização de tecnologia de gestão de estacionamento anteriormente reservada a grandes operadores, tornando-a acessível a pequenos e médios parques.

**ODS 11 — Cidades e Comunidades Sustentáveis**
Redução do tempo de procura de lugar de estacionamento e eliminação da dependência de hardware físico, contribuindo para uma mobilidade urbana mais fluida.

**ODS 17 — Parcerias para a Implementação dos Objetivos**
Integração via Stripe Connect permite transferências diretas entre condutores e operadores independentes, promovendo a descentralização económica.

<br/>

---

<br/>

<div align="center">

**Pedro Miguel Gonçalves Costa**

Prova de Aptidão Profissional
Técnico de Gestão e Programação de Sistemas Informáticos
Escola Profissional Ruiz Costa · 2023/2026

</div>
