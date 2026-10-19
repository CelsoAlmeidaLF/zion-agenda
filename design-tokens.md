# Studio Agenda — Design Tokens

> Extraído do canvas **"Studio Agenda — Telas do App"** (21 telas mobile, 390×844).
> Origem: valores literais encontrados nos arquivos `.dc.html` do projeto, agrupados e nomeados.
> Versão: 1.0 · 16/10/2026 · Autor: Celso de Almeida Leite Filho (Systekna)

---

## 1. Princípios visuais

| Princípio | Como aparece nas telas |
|---|---|
| Neutro e funcional | Fundo cinza muito claro, cartões brancos com borda fina, texto quase preto |
| Uma cor de marca, uma cor de ação | **Magenta** (`#c2255c`) identifica a marca e o item ativo; **Azul** (`#1c6fd1`) é ação/link/FAB |
| Cor = significado | Status do atendimento, profissional e forma de pagamento sempre têm cor própria |
| Tipografia pesada | Nunito Sans em pesos 800–900 para títulos, nomes e valores |
| Toque confortável | Linhas de lista de 62–66 px, FAB de 64 px, campos de 66 px |

---

## 2. Cores

### 2.1 Marca e ação

| Token | Valor | Uso |
|---|---|---|
| `--color-brand` | `#c2255c` | Cabeçalho do menu, aba ativa, borda de campo obrigatório, segmento ativo, badge de lembretes |
| `--color-action` | `#1c6fd1` | Links, FAB, botões de ação, ícones de editar |
| `--color-action-hover` | `#1558a8` | Hover/pressed de link e botão de ação |
| `--color-action-shadow` | `rgba(28,111,209,.6)` | Sombra colorida do FAB |
| `--color-danger` | `#d63b3b` | Encerrar sessão, ações destrutivas |

### 2.2 Neutros (texto)

| Token | Valor | Uso |
|---|---|---|
| `--text-primary` | `#15171c` | Texto principal, ícones |
| `--text-strong-2` | `#2a2d33` | Texto secundário em cartões de agendamento |
| `--text-secondary` | `#5a5d66` | Rótulos, cabeçalhos de cartão |
| `--text-muted` | `#6b6f78` | Subtítulos, legendas, sobretítulos (ex.: "Comanda") |
| `--text-placeholder` | `#7d8089` | Placeholder em itálico, filtros |
| `--text-disabled` | `#9a9da4` | Versão, chevrons, texto desabilitado |
| `--text-on-color` | `#ffffff` | Texto sobre marca, avatar, badge |

### 2.3 Neutros (superfície e borda)

| Token | Valor | Uso |
|---|---|---|
| `--surface-0` | `#ffffff` | Cartões, listas, folhas (sheets) |
| `--surface-1` | `#fafafa` | Fundo de telas de formulário |
| `--surface-2` | `#f3f3f5` | Fundo de telas de conteúdo |
| `--surface-header` | `#f0f0f2` | Barra superior, barra de data |
| `--surface-hover` | `#f5f5f7` / `#f7f7f9` | Hover de item de menu/lista |
| `--surface-input-muted` | `#e3e4e7` | Botão "Adicionar filtros" |
| `--surface-block` | `#e0e1e4` | Bloqueio de agenda |
| `--border-default` | `#dcdde1` | Divisores, bordas de cabeçalho |
| `--border-card` | `#d6d8dc` | Borda de cartões e campos |
| `--border-soft` | `#e3e4e8` | Divisor de opções em sheet |
| `--border-block` | `#b5b8be` | Borda do bloqueio |
| `--grid-line` | `#c9cbd0` | Linhas de hora na grade |
| `--badge-neutral` | `#9ea1a8` | Contadores (27 agendamentos, 5 comandas) |
| `--badge-zero` | `#dedfe2` | Saldo zerado do cliente |
| `--overlay` | `rgba(20,22,28,.45)` | Fundo atrás de bottom sheet / modal |

### 2.4 Status do atendimento

| Token | Valor | Status |
|---|---|---|
| `--status-marcado` | `#1eaee8` | Marcado |
| `--status-confirmado` | `#5b73c4` | Confirmado (também borda padrão do cartão na agenda; título `#3d58b3`) |
| `--status-espera` | `#f2c200` | Em espera |
| `--status-iniciado` | `#9ccf6b` | Iniciado |
| `--status-atrasado` | `#f08a24` | Atrasado |
| `--status-cancelado` | `#7d7f86` | Cancelado |
| `--status-pago` | `#16a34a` | Finalizado / Pago |
| `--status-pendente-flag` | `#e6c229` | Canto dobrado: pendência na comanda |

### 2.5 Profissionais (avatar + coluna)

| Profissional | Avatar | Anel / coluna | Fundo da coluna |
|---|---|---|---|
| Patrícia (Gerência) | `#2a8ad6` | `#2a8ad6` | `#e9f3fb` |
| Camila Rocha (Estética) | `#9a6fd0` | `#9a6fd0` | `#f6f1fb` |
| Juliana Prado (Cabelos) | `#6aae5c` | `#8cc97e` | `#f3f9f1` |
| Diego Martins (Cabelos) | `#4e8f42` | `#8cc97e` | — |
| Thaís Moura (Manicure) | `#2f9a83` | `#3aa58e` | — |
| Bianca Lopes (Manicure) | `#3aa58e` / `#c07a2c` | `#3aa58e` | — |
| Sueli Andrade (Manicure) | `#d08a3a` / `#a85a6e` | — | — |
| Recepção | `#b39a3e` | — | — |

Regra: anel = `box-shadow: 0 0 0 2.5px <anel>` sobre borda branca de 2 px. Anel por **área** (Manicure = teal, Cabelos = verde, Estética = roxo, Gerência = azul).

### 2.6 Financeiro

| Token | Valor | Uso |
|---|---|---|
| `--fin-positive` | `#3f9c3a` | Saldo final positivo |
| `--fin-income` | `#8a5ad6` | Rótulo "Entradas" |
| `--fin-income-icon` | `#8a6be0` | Ícone seta de entrada |
| `--fin-outcome` | `#c95fc9` | Rótulo "Saídas" |
| `--fin-outcome-icon` | `#e46fd8` | Ícone seta de saída |
| `--fin-commission-badge` | `#4caf50` | Saldo de comissão do profissional |
| `--pay-credit` | `linear-gradient(180deg,#4fb8ef,#2a8ad6)` + faixa `#1f3a5a` | Cartão de crédito |
| `--pay-cash` | `#16b85a` | Dinheiro |
| `--pay-pix` | `#e6e7ea` | Pix |
| `--whatsapp` | `#3fa34d` | Botão WhatsApp |

### 2.7 Padrões gráficos

| Token | Valor | Uso |
|---|---|---|
| `--pattern-unavailable` | `repeating-linear-gradient(135deg,#fff 0 6px,#9a9da4 6px 7.2px)` | Horário fora do expediente |
| `--pattern-hour-lines` | `repeating-linear-gradient(180deg,transparent 0 71px,#c9cbd0 71px 72px)` | Linhas da grade horária |

---

## 3. Tipografia

**Família única:** `'Nunito Sans', sans-serif` (Google Fonts, eixo `opsz 6..12`, pesos 400/600/700/800/900, itálico 400/600).

| Token | Tamanho | Peso | Uso |
|---|---|---|---|
| `--fs-display` | 38px | 900 | Hora em destaque (formulário) |
| `--fs-h1` | 30px | 900 | Horário na comanda |
| `--fs-h2` | 23px | 900 | Nome do cliente/profissional na ficha |
| `--fs-h3` | 20–21px | 900 | Título de cartão, valores de saldo, data na barra |
| `--fs-lg` | 19px | 400/900 | Item de menu, linhas de lista principais, valores |
| `--fs-md` | 18px | 400/900 | Opções de sheet, botões, valores de movimento |
| `--fs-base` | 16px | 400/800 | Corpo, título de tela, links |
| `--fs-sm` | 15–15.5px | 600/900 | Abas, nomes de coluna, rótulos |
| `--fs-xs` | 13–14.5px | 600/800 | Sobretítulo, legenda, cartão da agenda |
| `--fs-2xs` | 11–12px | 800 | Badges, contadores |
| `--fs-avatar-mini` | 9.5–10px | 800 | Iniciais em avatar de 26 px |

| Peso | Token | Uso |
|---|---|---|
| 400 | `--fw-regular` | Corpo |
| 600 | `--fw-semibold` | Nomes de coluna, links secundários |
| 700 | `--fw-bold` | Horário em cartão de agenda |
| 800 | `--fw-extrabold` | Sobretítulos, badges, links de ação |
| 900 | `--fw-black` | Títulos, nomes, valores |

Line-height: `1` em horas da grade, `1.15` no display, herdado (~1.35) no resto. Letter-spacing: `-.5px` só no display.

---

## 4. Espaçamento

Escala observada (px): **4 · 6 · 8 · 10 · 12 · 14 · 16 · 18 · 20 · 22 · 24 · 30**

| Token | Valor | Uso |
|---|---|---|
| `--space-1` | 4px | Gap mínimo, padding de ícone |
| `--space-2` | 8px | Gap entre ícone e texto |
| `--space-3` | 12px | Padding lateral de barra, gap de lista |
| `--space-4` | 14px | Padding de tela, gap entre cartões |
| `--space-5` | 16px | Padding de cartão |
| `--space-6` | 20px | Padding de campo |
| `--space-7` | 24px | Padding de item de menu |
| `--space-8` | 30px | Distância do FAB à borda inferior |

### Alturas fixas

| Token | Valor | Uso |
|---|---|---|
| `--h-appbar` | 70px | Barra superior |
| `--h-colhead` | 46px | Cabeçalho de colunas da agenda |
| `--h-hour` | 72px | 1 hora na grade (30 min = 36px) |
| `--h-list-item` | 62–66px | Item de menu, opção de sheet, campo |
| `--h-fab` | 64px | Botão flutuante |
| `--w-hour-gutter` | 46px | Coluna das horas |
| `--w-drawer` | 272px | Menu lateral |
| `--size-avatar-lg` | 56–58px | Avatar na ficha/menu |
| `--size-avatar-md` | 40–46px | Avatar em lista |
| `--size-avatar-sm` | 26px | Avatar em linha de serviço |
| `--size-icon` | 24–26px | Ícones |

---

## 5. Raios

| Token | Valor | Uso |
|---|---|---|
| `--radius-xs` | 3px | Badge de saldo, mini cartão de pagamento |
| `--radius-sm` | 5–6px | Cartão da agenda, segmento, botão de filtro |
| `--radius-md` | 8px | Cartões, campos, segmented control |
| `--radius-lg` | 10px | Cartão de resumo, cartão de horário |
| `--radius-xl` | 16px | Topo do bottom sheet |
| `--radius-pill` | 9px / 999px | Contadores |
| `--radius-full` | 50% | Avatar, FAB, botões redondos |
| `--radius-device` | 36px | Moldura do artboard (não usar no app) |

## 6. Bordas

| Token | Valor |
|---|---|
| `--border-hairline` | `1px solid var(--border-default)` |
| `--border-card` | `1.5px solid var(--border-card)` |
| `--border-field-required` | `1.5px solid var(--color-brand)` |
| `--border-appointment` | `1.5px solid <status>` + `border-left-width: 5px` |
| `--border-tab-active` | `3px solid var(--color-brand)` (aba) / `4px solid <prof>` (coluna) |

## 7. Elevação

| Token | Valor | Uso |
|---|---|---|
| `--shadow-fab` | `0 8px 20px -6px rgba(28,111,209,.6)` | FAB |
| `--shadow-drawer` | `6px 0 24px rgba(0,0,0,.18)` | Menu lateral |
| `--shadow-chip` | `0 1px 3px rgba(0,0,0,.25)` | Chips pequenos |
| `--ring-avatar` | `0 0 0 2.5px <cor da área>` | Anel do avatar |

## 8. Ícones

Traço (`stroke`) de **2–2.4 px**, `stroke-linecap: round`, `stroke-linejoin: round`, caixa 24×24, cor `currentColor`. Ícones sólidos só para cliente, equipe, filtro e telefone. Nunca emoji.

## 9. Componentes (anatomia)

| Componente | Especificação |
|---|---|
| **App bar** | 70px, fundo `--surface-header`, borda inferior hairline; título central com sobretítulo 13/800 muted + título 16–18/900 |
| **Cartão de agendamento** | Fundo branco, borda 1.5 da cor de status, borda esquerda 5px, raio 6, padding 5×8; hora 13/700, nome 13.5/800, serviço 13 |
| **Bloqueio** | Fundo `--surface-block`, borda `--border-block` |
| **Cartão** | Fundo branco, borda 1.5 `--border-card`, raio 8–10, padding 16×18 |
| **Linha de serviço** | Bolinha 10px de status · nome 16.5 · avatar 26px à direita |
| **Segmented control** | Contêiner borda 1.5 raio 8 padding 6; segmento ativo fundo marca + texto branco 17/900 |
| **Campo-seletor** | 66px, borda 1.5 marca, raio 8, placeholder itálico 20/600 `--text-placeholder` |
| **Bottom sheet** | Raio superior 16, cabeçalho `--surface-2`, opções de 62px com bolinha de cor à esquerda |
| **Aba** | 15.5/900 `--text-secondary`; ativa = marca + borda inferior 3px |
| **FAB** | 64px, círculo, `--color-action`, ícone + 28px, `--shadow-fab`, 22px da direita, 30px da base |
| **Badge contador** | Fundo `--badge-neutral`, branco, 11–12/800, raio pill |
| **Item de movimento** | Ícone 24px colorido + hora · tag 14.5/900 · título 16/900 · valor 19 alinhado à direita |

## 10. Breakpoints (adicionados para o MVP web)

| Token | Faixa | Layout |
|---|---|---|
| `--bp-mobile` | 0–599px | 1 coluna; app bar + drawer; 3 profissionais por vez na agenda (rolagem horizontal) |
| `--bp-tablet` | 600–1023px | Trilho lateral de ícones (72px); agenda com até 5 colunas |
| `--bp-notebook` | 1024–1439px | Menu lateral fixo (240px) com rótulos; todas as colunas |
| `--bp-wide` | ≥1440px | Menu lateral + conteúdo + painel de detalhe à direita (400px); conteúdo máx. 1680px |

---

## 11. CSS pronto

```css
:root{
  --color-brand:#c2255c; --color-action:#1c6fd1; --color-action-hover:#1558a8; --color-danger:#d63b3b;
  --text-primary:#15171c; --text-secondary:#5a5d66; --text-muted:#6b6f78; --text-placeholder:#7d8089; --text-disabled:#9a9da4;
  --surface-0:#fff; --surface-1:#fafafa; --surface-2:#f3f3f5; --surface-header:#f0f0f2; --surface-hover:#f5f5f7; --surface-block:#e0e1e4;
  --border-default:#dcdde1; --border-card:#d6d8dc; --border-soft:#e3e4e8; --grid-line:#c9cbd0; --badge-neutral:#9ea1a8;
  --status-marcado:#1eaee8; --status-confirmado:#5b73c4; --status-espera:#f2c200; --status-iniciado:#9ccf6b;
  --status-atrasado:#f08a24; --status-cancelado:#7d7f86; --status-pago:#16a34a;
  --fin-positive:#3f9c3a; --fin-income:#8a5ad6; --fin-outcome:#c95fc9;
  --font:'Nunito Sans',sans-serif;
  --radius-sm:6px; --radius-md:8px; --radius-lg:10px; --radius-xl:16px;
  --h-appbar:70px; --h-hour:72px; --h-fab:64px;
  --shadow-fab:0 8px 20px -6px rgba(28,111,209,.6); --shadow-drawer:6px 0 24px rgba(0,0,0,.18);
  --overlay:rgba(20,22,28,.45);
}
```

## 12. tokens.json (W3C Design Tokens)

```json
{
  "color": {
    "brand": {"$value": "#c2255c", "$type": "color"},
    "action": {"$value": "#1c6fd1", "$type": "color"},
    "action-hover": {"$value": "#1558a8", "$type": "color"},
    "text": {
      "primary": {"$value": "#15171c", "$type": "color"},
      "secondary": {"$value": "#5a5d66", "$type": "color"},
      "muted": {"$value": "#6b6f78", "$type": "color"}
    },
    "surface": {
      "0": {"$value": "#ffffff", "$type": "color"},
      "1": {"$value": "#fafafa", "$type": "color"},
      "2": {"$value": "#f3f3f5", "$type": "color"},
      "header": {"$value": "#f0f0f2", "$type": "color"}
    },
    "border": {
      "default": {"$value": "#dcdde1", "$type": "color"},
      "card": {"$value": "#d6d8dc", "$type": "color"}
    },
    "status": {
      "marcado": {"$value": "#1eaee8", "$type": "color"},
      "confirmado": {"$value": "#5b73c4", "$type": "color"},
      "espera": {"$value": "#f2c200", "$type": "color"},
      "iniciado": {"$value": "#9ccf6b", "$type": "color"},
      "atrasado": {"$value": "#f08a24", "$type": "color"},
      "cancelado": {"$value": "#7d7f86", "$type": "color"},
      "pago": {"$value": "#16a34a", "$type": "color"}
    }
  },
  "font": {"family": {"$value": "Nunito Sans, sans-serif", "$type": "fontFamily"}},
  "radius": {"sm": {"$value": "6px"}, "md": {"$value": "8px"}, "lg": {"$value": "10px"}, "xl": {"$value": "16px"}},
  "size": {"appbar": {"$value": "70px"}, "hour": {"$value": "72px"}, "fab": {"$value": "64px"}}
}
```
