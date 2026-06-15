# Plataforma de Gestão de Avaliações com IA (Smart Assessment)

![Next.js](https://img.shields.io/badge/Next.js-black?style=for-the-badge&logo=next.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![MUI](https://img.shields.io/badge/MUI-%230081CB.svg?style=for-the-badge&logo=mui&logoColor=white)

> **Status:** MVP Finalizado (Sprint 6) | **Contexto:** Engenharia de Software (UNIFESP)

## Sobre o Projeto

O **Sistema de Avaliação Inteligente** é uma solução fullstack desenvolvida para modernizar o ciclo de avaliações acadêmicas. O projeto ataca diretamente a ineficiência da correção manual e a dificuldade na personalização de ensino.

A plataforma utiliza **Inteligência Artificial (LLMs)** para auxiliar na criação criativa de questões e **Visão Computacional (OCR)** para automatizar a correção de gabaritos físicos, gerando analytics detalhados sobre o desempenho da turma em tempo real.


### Principais Diferenciais
* **Correção Automatizada:** Processamento de imagens de cartões-resposta (gabaritos) via upload.
* **Geração de Conteúdo via IA:** Integração com LLMs para criar enunciados, alternativas e distratores contextualizados.
* **Data-Driven:** Dashboards interativos para professores identificarem lacunas de aprendizado.
* **Exportação LaTeX:** Geração automática de provas formatadas em PDF prontas para impressão.

---

## Documentação do Projeto

O projeto seguiu a metodologia Ágil (Scrum) ao longo do semestre. Detalhes sobre todo o projeto e suas funcionalidades detalhadas podem ser consultados na apresentação oficial:

📄 **[Ver Apresentação Completa do Projeto (PDF)](./docs/Engenharia%20de%20Software%20Equipe%20Golf.pdf)**

---

## Tecnologias e Arquitetura

O projeto segue uma arquitetura moderna baseada em microsserviços containerizados.

* **Frontend:** Next.js (App Router), Material UI (MUI) para interface responsiva e Recharts para visualização de dados.
* **Backend & AI:** Next.js API Routes, LangGraph (Orquestração de LLMs) e integração com OpenAI API.
* **Banco de Dados:** MongoDB Atlas (NoSQL) para flexibilidade de schemas de provas e questões.
* **Infraestrutura:** Docker e Docker Compose para orquestração de containers.

### Arquitetura do Sistema
<img width="100%" alt="Arquitetura do Sistema" src="https://github.com/user-attachments/assets/e005443e-e1eb-4ee0-b4d6-0d204bcb5549" />


---


## Funcionalidades Detalhadas

### Para Professores (Módulo de Gestão)
1.  **Auxílio de IA:** Uso de LLMs para auxiliar na criação de enunciados, sugerir alternativas e distratores.
2.  **Montagem de Provas:** Seleção de questões e diagramação automática em LaTeX/PDF.
3.  **Correção em Lote:** Upload de fotos das provas realizadas; o sistema identifica o aluno e computa a nota automaticamente.
4.  **Dashboard de Turma:** Análise estatística de erros e acertos por questão e por aluno.

### Para Alunos (Módulo de Aprendizado)
1.  **Feedback Imediato:** Acesso às notas e correções assim que processadas.
2.  **Métricas de Aprendizado:** Acompanhamento individual de métricas baseadas nas atividades submetidas na plataforma.
3.  **Listas Personalizadas:** Criação de listas de exercícios de uma base de dados personalizadas com base no desempenho do aluno.

---

## Como Rodar o Projeto

### Pré-requisitos
* Docker e Docker Compose instalados.
* Git instalado.

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/brenonak/sistema-avaliacao-inteligente.git](https://github.com/brenonak/sistema-avaliacao-inteligente.git)
   cd sistema-avaliacao-inteligente

2. **Configure as Variáveis de Ambiente:**
Renomeie o arquivo `.env.example` para `.env` e insira suas credenciais (MongoDB, OpenAI Key, etc).
3. **Inicie com Docker:**
```bash
docker-compose up --build

```


*O build inicial pode levar alguns minutos.*
4. **Acesse a Aplicação:**
Abra seu navegador em `http://localhost:3000`.

---

## Estrutura do Repositório

```text
/sistema-avaliacao-inteligente
├── docs/                  # Documentação e artefatos do Scrum
├── src/
│   ├── app/               # Rotas e Páginas (Next.js App Router)
│   ├── components/        # Componentes Reutilizáveis (MUI)
│   ├── lib/               # Configurações de Banco e Utils
│   └── services/          # Integrações com IA e Lógica de Negócio
├── public/                # Assets estáticos
├── docker-compose.yml     # Orquestração dos containers
└── README.md

```

---

## Deploy

* **Deploy de Produção:** [Acessar Demonstração](https://es-local.vercel.app/)

---

<p align="center">
Desenvolvido por <strong>Estevan Santos</strong> e equipe durante a disciplina de Engenharia de Software.
</p>
