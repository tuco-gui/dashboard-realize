# Dashboard Realize — Alea Botucatu

Relatório executivo no padrão do Ortega, com abas Visão Geral, Campanhas, Funil/CRM, Diagnóstico e Fontes. Corte 27/10 a 08/11/2026.

**Fontes verificadas em 09/11:** Meta Ads conta 257842684035643 (R$ 450,26, 42 conversas iniciadas, 24.870 impressões e 495 cliques), Google Ads conta 368-346-8864 (R$ 492,06, 16 cadastros da planilha atribuídos ao Google, 8 registros alea_form_success da plataforma já incluídos, 4 eventos secundários de encaminhamento WhatsApp, 1.498 impressões e 190 cliques), Google Sheets Realize `Leads Alea` (16 registros de entrada, não deduplicados).

**Atenção:** conversas Meta, 16 cadastros Google da planilha incluem os eventos de formulário do Ads; 4 encaminhamentos WhatsApp Google são eventos secundários, potencialmente sobrepostos. Não representam 62 leads únicos nem devem ser somados. Qualificação, visitas, vendas e retorno comercial permanecem “Não apurado” até validação no Superlógica.

**Contexto específico Realize:** Alea é o empreendimento da Tenda; Realize faz atendimento/comercialização. Formulário e minichat alimentam planilha e Harvest/Superlógica. Precisam preservar renda, UTMs e protocolo. A distribuição aos corretores depende de configuração de times/roleta; comentário não garante atribuição ao Sylvio. Remarketing teve gasto efetivo registrado no período, embora o planejamento inicial previsse deixá-lo pausado.

**Técnica:** Site estático em `index.html`, sem segredos e sem dados pessoais. Filtro de datas usa granularidade diária; tabela por criativo mostra somente o período integral. Exportação em PDF pelo navegador. Esta é uma captura das APIs, não feed em tempo real. Validar proteção de acesso antes de compartilhar externamente.

**Evolução:** sincronização autenticada e reconciliação de contato único/protocolo/etapas comerciais; não inventar vendas ou leads qualificados.

## Edição ampliada — 09/11/2026

- Identidade visual: cabeçalho branco; logomarcas oficiais da Figueira Marketing e Realize (branca sobre placa azul), ambas recuperadas do repositório público `tuco-gui/alea-botucatu`. Sem vermelho fora da própria marca da Figueira. Paleta azul, verde e tons neutros.
- Campanhas: filtro visual `Visão geral`, `Google Ads`, `Meta Ads`, anúncios Meta e palavras-chave/termos efetivos da Pesquisa paga Google.
- Analytics GA4: propriedade `561083509`, 27/10 a 08/11/2026: 114 sessões, 92 usuários únicos, 149 visualizações, 65 sessões engajadas (57,02%). Google/CPC responde por 100 sessões. Séries diárias e origem/mídia.
- Search Console: `sc-domain:casasaleaembotucatu.com.br`, 27/10 a 08/11: 8 impressões orgânicas, 0 cliques. Consultas detalhadas somam 7 impressões; 1 não aparece no recorte por consulta. URL com impressões: `/realize.html`.
- Google Ads: palavras-chave e termos de pesquisa vêm da conta 368-346-8864. Conversões das palavras-chave são eventos atribuídos pela plataforma, não vendas nem distribuição dos 16 cadastros comerciais, que continuam conciliados pela planilha.
- Os dados foram verificados contra APIs e são um recorte publicado; para atualizações automáticas, criar integração autenticada com verificação de proveniência e filtros por período.

## Revisão de layout baseada no relatório Ortega (09/11/2026)
- Visão Geral Executiva na mesma estrutura de leitura do Ortega: investimento do período, métricas de mídia, resultado comercial acumulado, investimento versus captações e alertas/análise.
- Mensalidade de agência Realize **R$ 750,00/mês**, informada pelo contratante. Agência pró-rata = mensalidade x dias corridos selecionados / 30; demonstrativo proporcional, não fatura ou confirmação da data de início contratual. Ferramentas de IA: valor **não informado**, não adicionar como zero nem ocultar do custo faltante. O "total conhecido" inclui mídia + agência proporcional, exclui ferramenta sem valor.
- Resultado comercial: não foram fornecidos/conciliados quantidades de qualificados, oportunidades, visitas, vendas e VGV; mostrar **não apurado**, sem usar zeros ou copiar projeções e indicadores do Ortega.
- Funil e Projeção: captações por canais separadas, próximas etapas dependentes da deduplicação e da evolução real no Superlógica; não aplicar benchmarks de imóveis alto padrão ao lançamento Alea.
- Abas complementares preservadas: Campanhas (Google / Meta, investimento por dia, evento de captação, tabelas, termos e anúncios), Analytics (GA4), Orgânico (GSC), Diagnóstico e Fontes.
- Seleção de intervalo: 7, 15, 30, 60, 90 e 180 dias, tudo e datas personalizadas. A disponibilidade é limitada pelo recorte das fontes (27/10 a 08/11).
- Logo Realize: imagem **azul oficial aprovada**, proveniente de `assets_aprovados/logo-realize-oficial-azul.jpg` no repositório Alea. Substitui a marca branca incorreta; manter apenas a identidade aprovada.
- Paleta de interface: branco, azul, verde e cinza, sem vermelho fora do logotipo Figueira.

## Atualização diária automatizada (09/11/2026)

### Contrato de dados
O HTML usa `fetch('/data/realize.json')` no navegador, sem credenciais, com `cache: no-store`. O arquivo JSON contém apenas métricas agregadas e metadados de frescor, nunca leads identificáveis ou tokens. Em caso de falha de download ou esquema incompleto, mostra o último recorte embutido e sinaliza que está desatualizado.

### Caminho de atualização
Tarefa agendada na nuvem (fuso **America/Sao_Paulo**) consulta APIs autorizadas Meta, Google Ads, GA4, Search Console e Google Sheets (Realize/Alea). Atualiza somente `data/realize.json` em `main` via GitHub, após validação de conteúdo. O Git push em `main` dispara automaticamente novo deploy Vercel no projeto `dashboard-realize`. Validação obrigatória do novo deploy `target=production, state=READY`.

### Fonte por campo
- `metaDaily` e `ads`: Marketing API Meta, conta `257842684035643`. Evento `onsite_conversion.messaging_conversation_started_7d`.
- `googleDaily`: Google Ads, cliente `3683468864`, custos em BRL (converter `costMicros / 1e6`), impressões/cliques/conversões com intervalo exato e granularidade diária.
- `formDaily`: Sheets `1vPQBhcAykwaM22t-8paKFXC42SGR1vnSf6hQls6ckqE`, aba `Leads Alea`, coluna de data `Recebido em`, canais Google na própria planilha; usar datas Brasil e registros por protocolo quando possível. **Não exportar dados pessoais.**
- `ga4Daily`, `ga4Sources`, `ga4Users` etc.: propriedade GA4 `561083509`.
- `gscDaily` e `gscQueries`: `sc-domain:casasaleaembotucatu.com.br`, respeitar atraso de disponibilidade de Search Console.
- `adsKeywords`, `adsSearchTerms`: métricas da campanha Google Ads `24406912922`; conversões nas tabelas significam eventos atribuídos e não vendas.
- `googleWhatsappSecondaryTotal`: ação secundária `alea_whatsapp_handoff`, usar `allConversions`, sem somar a cadastros.
- Valores comerciais `qualified`, `opportunities`, `visits`, `sales` e `vgv`: `null` até comprovação por CRM Superlógica ou declaração verificada; não copiar nem estimar resultados Ortega.
- `agencyMonthly`: R$ 750,00, informação contratual do usuário; `aiToolsMonthly`: `null` até valor autorizado.

### Regras de segurança
1. Cliente Realize isolado; não misturar contas, dados ou leads de outros clientes.
2. Atualizar recorte `periodEnd` até o último dia encerrado; manter histórico desde `periodStart`.
3. Validar datas, moeda, totais e shape de todas as séries antes de publicar.
4. Se uma fonte falhar, manter os valores anteriores dela, marcar `sources.<fonte>.status='error'` e `dataThrough` original; não inventar zeros.
5. Só atualizar `generatedAt` após persistir o novo snapshot (na mesma operação).
6. Conferir deploy da Vercel após commit; reportar erro se não estiver READY.
7. Interface sinaliza data do snapshot e fontes pendentes. Snapshots não são necessariamente atualização em tempo real e fontes podem ter atrasos de atribuição.
