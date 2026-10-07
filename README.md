# MentoraAcessível - MVP de Agendamento e Consultoria

> Aplicação desenvolvida como MVP para validação de tese de mercado baseada em uma dor real, aplicando os conceitos de **Design Universal** e IA como co-founder.

---

## 📸 Evidências e Telas

<img width="1378" height="863" alt="Captura de tela 2026-10-06 160701" src="https://github.com/user-attachments/assets/8344eccb-8d48-4d1d-bb40-d72bd13e4f18" />

<img width="1365" height="481" alt="Captura de tela 2026-10-06 160721" src="https://github.com/user-attachments/assets/37c48047-8842-4a42-bbd3-d629fc7632b0" />

<img width="1365" height="855" alt="Captura de tela 2026-10-06 160735" src="https://github.com/user-attachments/assets/7ad92be8-2e06-4059-9a8d-5b2d0d0d10d9" />

<img width="1041" height="861" alt="Captura de tela 2026-10-07 141953" src="https://github.com/user-attachments/assets/e302caff-668a-4a89-8cde-10fd9695c14c" />


- **Aplicação Publicada:** https://pixel-perfect-showcase-22251.lovable.app
- **Repositório GitHub:** `https://github.com/Lehhest/DESAFIO-DIO---organizador-e-agendador-de-consultorias-mentorias-r-pidas-por-LOVABLE`

---

## 1. A Dor Escolhida e a Oportunidade de Negócio
A dificuldade que muitos estudantes e profissionais têm em encontrar suporte técnico pontual ou mentoria de carreira sem passar por processos burocráticos ou utilizar plataformas com baixa acessibilidade digital. 

A solução oferece uma interface minimalista, totalmente focada em **Design Universal**, que permite escolher a área de suporte e iniciar o agendamento em poucos cliques.

---

## 2. Conceito de Design Universal Aplicado
Para garantir que a aplicação possa ser utilizada com excelente experiência por qualquer pessoa:
- **Navegabilidade:** Total suporte a navegação por teclado (`TAB` e atalhos).
- **Legibilidade:** Contraste elevado (WCAG 2.1 AA), suporte a modo claro/escuro e fontes em tamanhos adequados.
- **Semântica e Leitura de Tela:** Tags HTML5 semânticas e atributos `aria-*` em componentes interativos.
- **Simplicidade:** Redução de barreiras de entrada e feedbacks claros sobre cada ação do formulário.

---

## 3. Tamanho de Mercado e Business Model Canvas

### Mercado (TAM, SAM, SOM)
- **TAM:** Mercado Global de EdTech e Mentorias Online.
- **SAM:** Estudantes e Profissionais de Tecnologia do Brasil (~R$ 150M).
- **SOM:** 500 agendamentos nos primeiros 6 meses (~R$ 45k).

### Business Model Canvas
- **Proposta de Valor:** Agendamento rápido de mentorias com acessibilidade universal e atendimento direto.
- **Canais:** Web App (Lovable) + Fechamento via WhatsApp.
- **Fonte de Receita:** Cobrança por sessão efetuada via PIX/WhatsApp.

---

## 4. Tese do MVP e Processos Manuais

### A Tese
Usuários que precisam de suporte pontual preferem a simplicidade de preencher um formulário simples e direto e fechar os detalhes via conversa no WhatsApp em vez de usarem plataformas complexas.

### O que ficou manual de propósito
- Envio do link de pagamento (PIX).
- Envio do link da sala de conferência (Google Meet).
- Confirmação final da agenda na planilha interna do mentor.

---

## 5. Mega Prompt Utilizado
# MEGA PROMPT: Aplicação MentoraAcessível (MVP)

Crie uma aplicação web responsiva e acessível (Design Universal) utilizando Lovable Cloud para o back-end de armazenamento de leads e agendamentos.

## 1. Princípios de Design Universal e Acessibilidade
- **Acessibilidade WCAG 2.1 AA:** Alto contraste de cores (modo claro/escuro nativo), fontes legíveis (mínimo 16px para texto base), suporte total a navegação via teclado (`tabindex` lógico e estados `:focus` destacados).
- **Semântica HTML:** Uso estrito de tags `<header>`, `<main>`, `<nav>`, `<section>`, `<footer>` e rótulos `aria-label` em todos os elementos interativos.
- **Formulários Acessíveis:** Labels claros para cada input, mensagens de erro descritivas e ajuda em texto.

## 2. Cores e Estilo
- **Cor Primária:** Azul Escuro Profundo `#1E3A8A` (Alta legibilidade).
- **Cor Secundária / Destaque:** Amarelo Âmbar `#D97706` (Para botões de ação e alertas visualmente distintos).
- **Fundo:** Off-white `#F8FAFC` no modo claro e `#0F172A` no modo escuro.

## 3. Funcionalidades da Aplicação

### A. Landing Page Pública (Cliente)
- **Cabeçalho:** Logo textualmente legível, botão de alternância de contraste e link direto para o formulário ("Ir para Agendamento").
- **Hero Section:** Título principal claro ("Sua mentoria rápida e sem barreiras"), subtítulo explicativo e CTA chamativo para o formulário.
- **Benefícios:** Lista em 3 cards informando facilidade, acessibilidade e suporte direto.
- **Formulário de Agendamento (Passo a Passo Interativo):**
  - Passo 1: Nome completo e E-mail.
  - Passo 2: Seleção da Área da Mentoria (Dropdown acessível).
  - Passo 3: Escolha de Data e Horário preferencial.
  - Passo 4: Campo de texto para explicar a principal dúvida/dor.
- **Ação do Formulário:** Ao enviar, salvar o registro no banco de dados do Lovable Cloud e redirecionar automaticamente o usuário para um link de WhatsApp com a mensagem pré-formatada contendo os dados do agendamento.

### B. Painel de Administração (`/admin`)
- Protegido por uma visualização de gestão de dados.
- **Tabela Acessível de Leads e Agendamentos:**
  - Listagem com: Nome, E-mail, Área, Data/Hora solicitada, Status (Pendente/Confirmado) e Ações.
  - Filtro simples por status.
  - Botão para "Alterar Status" e "Abrir conversa do WhatsApp com o cliente".
  - Quadro explicativo de métricas simples (Total de agendamentos, Pendentes e Concluídos).

Gere o código completo mantendo o código limpo, componentes reutilizáveis e performance otimizada.

---

## 6. Estrutura do Repositório

├── src/
│   ├── components/      # Componentes acessíveis da UI
│   ├── pages/           # Landing Page e Painel Admin
│   └── lib/             # Integração com Lovable Cloud
├── public/              # Ativos estáticos
└── README.md            # Documentação completa do projeto

---

## 7. Checklist de Submissão
- [x] Aplicação publicada e acessível publicamente.
- [x] Repositório público com código-fonte completo.
- [x] Sem chaves, tokens ou credenciais salvas no código.
- [x] Nome do repositório em minúsculas e sem caracteres especiais (`DESAFIO-DIO---organizador-e-agendador-de-consultorias-mentorias-r-pidas-por-LOVABLE`).
