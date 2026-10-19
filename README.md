# Studio Agenda · PWA

> Agenda de atendimentos, comandas, caixa e comissões para estúdios de beleza e salões.

Aplicação de página única (SPA) instalável (*Progressive Web App*), desenvolvida em HTML5, CSS3 moderno e JavaScript puro (*Vanilla ES Modules*), operando em arquitetura **Local-First** com zero dependências externas de build.

## Demonstração Online
Acesse a versão em produção via GitHub Pages:
👉 **[https://celsoalmeidalf.github.io/studio-agenda/](https://celsoalmeidalf.github.io/studio-agenda/)**

---

## Funcionalidades
- **Agenda em Grade:** Visualização por dia com colunas por profissional e intervalos de 30 minutos.
- **Comandas e Atendimentos:** Abertura, inclusão de múltiplos serviços e acompanhamento de status.
- **Caixa Diário e Fechamento:** Controle de entradas, saídas, descontos, gorjetas e saldo inicial.
- **Cálculo de Comissões:** Percentual configurável por profissional com baixa de pagamentos.
- **Cadastro Completo:** Clientes com histórico de agendamentos e catálogo de serviços.
- **Local-First & Offline:** Totalmente funcional sem conexão via Service Worker e persistência local (`localStorage`).
- **Backup e Restauração:** Exportação e importação integral da base em arquivo JSON.

---

## Design System
Especificação visual baseada no documento [design-tokens.md](design-tokens.md):
- **Paleta de Marca:** Magenta (`#c2255c`) e Azul de Ação (`#1c6fd1`).
- **Tipografia:** Nunito Sans (pesos 400 a 900).
- **Iconografia:** Vetorial SVG em padrão Lucide (24x24).
