# 👩‍💼 Patricia - Assistente Virtual Inteligente (SEDEAD)

![Status](https://img.shields.io/badge/status-Production-green)
![Architecture](https://img.shields.io/badge/architecture-Microservices-blue)
![Deploys](https://img.shields.io/badge/deploy-GitHub%20Actions-2088FF)

**Patricia** é a solução de inteligência artificial desenvolvida para auxiliar os colaboradores da **SEDEAD** (Secretaria de Estado da Administração). O objetivo é agilizar processos internos, desburocratizar o acesso a normativas e aumentar a eficiência operacional do órgão através de interfaces conversacionais.

---

## 🏛️ Visão Geral da Solução

O projeto não é um monólito, mas sim um ecossistema de microsserviços distribuídos, projetados para alta disponibilidade e tolerância a falhas.

### O Ecossistema (Repositórios)

A solução é composta por **5 repositórios** interconectados:

* 📱 **[service-flutter]**: Frontend Mobile/Web (Acesso do usuário via HTTPS/443).
* ☕ **[service-java]**: Microsserviço Backend (API Rest).
* 🤖 **[service-csharp]**: Microsserviço Backend (Processamento e Integração).
* ⚙️ **[service-devops]**: Infraestrutura como Código (Terraform), e Automação.
* 🧠 **[project-core]**: Repo central para organização dos microsserviços.

---

## 🚀 Arquitetura de Alto Nível

O tráfego é gerenciado de forma segura e escalável:

1.  **Client:** O usuário acessa a aplicação Flutter via camada segura (Porta 443).
2.  **Edge:** Um Load Balancer (ALB) distribui a carga.
3.  **Compute:** Os serviços Java e C# rodam isolados em containers (Porta 8080) dentro de uma rede privada na AWS.
4.  **Automação:** Não há deploy manual. Qualquer alteração de código passa por pipelines rigorosos de CI/CD.

---

## 🛠️ Stack Tecnológica

* **Frontend:** Flutter
* **Backends:** Java & C# (.NET)
* **Cloud Provider:** AWS (Amazon Web Services)
* **Orquestração:** Amazon ECS (Fargate)
* **Pipeline:** GitHub Actions
* **Infraestrutura:** Terraform

---
