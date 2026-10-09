# 🏎️ Porsche Sales Intelligence - Dashboard Executivo de Vendas

Dashboard interativo desenvolvido para análise executiva de desempenho das vendas da base sanitizada da Porsche, combinando filtros dinâmicos em tempo real, visualização de indicadores (KPIs), perguntas de negócio automatizadas e recomendações estratégicas.

---

## 🔗 Links do Projeto

- 🚀 **Dashboard Publicado (GitHub Pages):** https://gabiconx.github.io/dashboard_porsche_sales/
- 📂 **Repositório do Código-Fonte:** https://github.com/Gabiconx/painel_vendas_porsche 

---

## 🎯 Perguntas de Negócio Analisadas

A dashboard responde automaticamente a três perguntas principais de negócio, que recalculam dinamicamente conforme os filtros aplicados:

1. **Qual o mês de maior venda da Porsche ao longo do período?**
   - *Finalidade:* Mapear a sazonalidade e picos de demanda para otimização de campanhas comerciais e planejamento de estoque.
2. **Em qual cidade foram vendidas mais Porsches?**
   - *Finalidade:* Identificar os principais polos geográficos de demanda para ações regionais, eventos de relacionamento e alocação de veículos.
3. **Qual o modelo de Porsche mais comprado?**
   - *Finalidade:* Entender a preferência e o mix de produto dos clientes para direcionamento de catálogo e estratégias de upsell.

---

## ⚙️ Tratamento de Dados e Sanitização

A base de dados foi tratada a partir da aba *Sanitized* da planilha oficial da Porsche:
- **Remoção de Inconsistências:** Isolamento dos registros com datas classificadas como `INVALID`, os quais foram desconsiderados nas análises temporais (gráfico mensal e pergunta de mês pico), mas mantidos nos indicadores gerais e na tabela detalhada.
- **Tipagem de Dados:** Normalização de preços (`price`) e milhagens (`mileage`) para valores numéricos puros, garantindo cálculos exatos de receita, ticket médio e milhagem média.
- **Integração:** Inclusão dos dados sanitizados em formato JSON diretamente dentro do arquivo `index.html` único, eliminando dependências externas e garantindo execução *standalone* no navegador sem servidor de backend.

---

## 🤖 Uso de IA e Metodologia de Desenvolvimento

O projeto foi desenvolvido em colaboração com IA (ChatGPT), utilizando uma abordagem iterativa de refinamento:

1. **Estrutura Inicial:** Solicitação dos componentes de filtros (Ano, Preço Máximo, Estado/Cidade encadeados, Modelo e Milhagem) e seções de KPIs/gráficos.
2. **Identidade Visual Premium (UI/UX):** Refinamento da interface com inspiração no portal oficial da Porsche Brasil (`porsche.com/brazil/pt/`), aplicando uma paleta minimalista em tons de branco, grafite e vermelho Porsche, tipografia *clean* e cartões executivos.
3. **Mapeamento de Imagens Dinâmicas:** Implementação de lógica JS para alteração automática da imagem fotográfica realista do veículo de acordo com o modelo/família selecionado (911, 718, Taycan, Panamera, Macan e Cayenne), acompanhada de links diretos para as páginas oficiais da marca.
4. **Refinamento Funcional:** Ajustes no fluxo de filtros (remoção do filtro lateral de mês para manter a granularidade limpa por Ano, mantendo o detalhamento de meses no gráfico e na tabela) e inclusão da seção automática de **Insights de Venda** (Comportamento, Geografia e Preço) atualizados a cada filtragem.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 / CSS3:** Layout responsivo, CSS Variables e estilização inspirada no ecossistema da Porsche.
- **JavaScript (Vanilla):** Manipulação de DOM, mecanismos de filtragem encadeada em tempo real e agregação de dados no cliente.
- **GitHub Pages:** Hospedagem estática do dashboard.
