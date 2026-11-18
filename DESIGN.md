# Design do site — Studio Marli Ventura

Referência visual: protótipo rosa (blocos arredondados, tons de blush/rosa, botões chocolate). Tipografia: **Roboto**. Sem cores neon, sem brilhos (glow) e sem gradientes chamativos.

## Paleta (tokens em `tailwind.config`, prefixo `mv-`)
| Token | Hex | Uso |
|---|---|---|
| `page` | `#FFF6F7` | fundo geral |
| `soft` | `#FCE9EC` | seções alternadas, cartões suaves |
| `blush` | `#F8DCE2` | painéis principais (hero, contato) |
| `petal` | `#F0C5CE` | selos, ícones, realces |
| `line` | `#EBC9D0` | bordas |
| `deep` | `#9C4259` | links, destaques, foco |
| `ink` / `choc` | `#3A2A2E` | texto principal e botão principal |
| `muted` | `#654C53` | texto secundário |
| `footer` | `#33242A` | rodapé |
| `ok` / `okBg` | `#2B6F4E` / `#E1F0E7` | status "aberto agora" |

Todos os pares de texto/fundo usados têm contraste ≥ 4,5:1 (WCAG AA). O dourado das estrelas (`gold`) é só decorativo e vem sempre acompanhado de texto.

## Componentes
- **Botão principal:** pílula chocolate (`bg-mv-choc`), texto claro. **Secundário:** pílula com borda chocolate. Alvos de toque ≥ 44 px.
- **Cartões:** cantos `28px`, fundo `soft`/`blush`/branco, borda `line`.
- **Rótulos de seção:** caixa-alta pequena em `deep`; títulos em Roboto 900 com tracking negativo.

## Heurísticas de Nielsen — onde cada uma aparece
1. **Visibilidade do status:** selo "Aberto agora / Fechado" calculado no horário de Brasília; menu destaca a seção atual; avisos (toast) ao abrir o WhatsApp, copiar ou salvar cookies; cabeçalho ganha sombra ao rolar.
2. **Mundo real:** linguagem simples (ex.: "tratamentos com luz e ozônio" ao lado de "fotoativação"); "Como chegar" em vez de "Localização"; mensagens de WhatsApp já escritas em português.
3. **Controle e liberdade:** "Desfazer" após salvar cookies; Esc fecha menu e modal; botão Cancelar; voltar ao topo.
4. **Consistência:** um único estilo de botão por função; todo link de agendamento diz "Agendar no WhatsApp"; mesma lista no menu e no rodapé.
5. **Prevenção de erros:** escolha do tratamento monta a mensagem antes de abrir o WhatsApp; prévia visível; links externos com `rel="noopener"` e aviso "abre em nova aba"; horário sempre em Brasília.
6. **Reconhecimento:** menu no celular (antes não existia), passos numerados 1 e 2 no agendamento, rótulos visíveis em todos os ícones, telefone e endereço sempre à vista.
7. **Eficiência:** link "Ir para o conteúdo", `tel:` para ligar em um toque, botões "Copiar número/endereço", menu fixo.
8. **Minimalismo:** removidos cartão duplicado de tratamento, relógio com segundos, estatística sem número, botão flutuante repetido, selo "Web App Oficial" e brilhos decorativos.
9. **Erros claros:** imagem que falha mostra aviso amigável (logo cai para o ícone local); falha ao copiar explica o que fazer; se o WhatsApp não abrir, o número aparece para ligar.
10. **Ajuda:** seção "Dúvidas frequentes" (agendar, avaliação, pagamento, endereço, atalho no celular) e política de privacidade acessível no rodapé.
