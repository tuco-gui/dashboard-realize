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
