# 📚 Sistema de Estudos de Língua Portuguesa para Concursos
### Foco: Educação Infantil e Licenciaturas (Pernambuco & Bancas Nacionais)

Aplicação Web SPA (Single Page Application) moderna, responsiva e rápida, desenvolvida em **React 18**, **TypeScript**, **Tailwind CSS**, **Recharts** e **Vite**, projetada especificamente para concurseiros da área educacional de Pernambuco.

---

## 🚀 Como Executar o Projeto

```bash
# 1. Instalar dependências (já realizado no ambiente)
npm install

# 2. Iniciar o servidor de desenvolvimento
npm run dev

# 3. Compilar para produção
npm run build
```

Acesse a aplicação no navegador em: `http://localhost:5173/` (ou na porta informada pelo Vite).

---

## 🏛️ Categorização Oficial das Bancas Examinadoras

Todo o acervo do sistema é estruturado em **provas reais de concursos oficiais já aplicados** (zero dados fictícios):

### 1. Bancas Foco PE
- **UPENET/IAUPE** (Concursos Caruaru, SEE-PE, Paulista, Olinda, Jaboatão dos Guararapes, Serra Talhada)
- **ADM&TEC** (Santa Cruz do Capibaribe, Camaragibe, Belo Jardim, Brejo da Madre de Deus)
- **FACAPE** (Petrolina, Cabrobó, Sertão do São Francisco)
- **IGEDUC** (Garanhuns, Arcoverde, Vitória de Santo Antão)
- **FADE/UFPE** (Universidade Federal de Pernambuco - TAE/Pedagogos)
- **ASPERHS** (Consórcios municipais e prefeituras do Agreste)
- **COVEST/COMPERVE** (Colégio de Aplicação da UFPE / Licenciaturas)

### 2. Bancas Nacionais Frequentes em PE
- **IBFC** (SEE-PE, Goiana, EBSERH-PE)
- **FGV** (Prefeitura do Recife, SEE-PE, Tribunais PE)
- **Cebraspe/CESPE** (Recife Educação, SEDUC, FNDE)
- **FCC** (Redes municipais de grande porte e tribunais regionais)
- **Instituto AOCP** (SEE-PE, Câmaras municipais de PE)
- **IDECAN** (Prefeituras e Educação Básica no Nordeste)
- **Consulpam** (Prefeituras do interior de Pernambuco)

---

## 📂 Arquitetura das 4 Áreas Fundamentais

### 1. 📚 Apostila & Resumos (Visão Geral)
- 11 módulos didáticos completos cobrindo:
  1. *Compreensão e Interpretação de Texto* (extrapolação, redução, coesão, anáfora/catáfora)
  2. *Crase* (regras práticas, troca pelo masculino "AO", casos proibidos e casos facultativos)
  3. *Concordância Verbal e Nominal* (verbos impessoais HAVER e FAZER, partícula apassivadora SE vs IIS)
  4. *Regência Verbal e Nominal* (verbos campeões: Assistir, Aspirar, Visar, Implicar, Preferir, Lembrar/Esquecer)
  5. *Pontuação* (ordem direta SVC, proibições de vírgula, vocativo, aposto explicativo e adjuntos deslocados)
  6. *Acentuação Gráfica* (Novo Acordo Ortográfico, paroxítonas com ditongos abertos, regra dos hiatos e proparoxítonas)
  7. *Morfologia & Classes de Palavras* (funções do QUE e do SE, valores semânticos de preposições e conjunções)
  8. *Colocação Pronominal* (próclise, mesóclise, ênclise e palavras atrativas)
  9. *Sintaxe do Período* (sujeito, predicado, complemento nominal vs adjunto adnominal)
  10. *Tipologia e Gêneros Textuais* (foco em educação infantil, textos instrucionais e dissertações)
  11. *Ortografia Oficial* (os 4 Porquês, parônimos, paralisar vs paralisia, exceção, privilégio)
- Destaques visuais para **"Cai Muito em Prova"** e **"Dicas da Banca PE"**.
- Botão direto para **"Praticar Questões deste Assunto"**.

### 2. 📖 Dicionário de Gramática & Conceitos Detalhados
- Guia em 4 etapas estruturadas para cada termo gramatical:
  1. **Definição Clara e Direta:** O que é o termo.
  2. **Como Identificar:** Regras, macetes mnemônicos e passo a passo lógico.
  3. **Como Usar Corretamente:** Casos obrigatórios e erros comuns a evitar.
  4. **Exemplos Reais de Concursos:** Frases de provas da IAUPE, FGV, IBFC, FACAPE, ADM&TEC com justificativa oficial da banca.
- Barra de busca instantânea e filtros por categorias morfológicas e sintáticas.

### 3. 📝 Módulo de Questões e Simulado
- **Filtros Personalizados:**
  - Seleção por tema único ou múltiplos temas simultaneamente.
  - Filtro por Bancas Foco PE vs Bancas Nacionais.
  - Quantidade por sessão: 10, 20, 50 ou Todas.
- **Modos de Estudo:**
  - **Modo Treino:** Feedback imediato ao clicar na alternativa com a explicação completa do gabarito.
  - **Modo Simulado Real:** Estilo dia de prova, sem revelação prévia, com cálculo de nota e tempo ao final.
- **Garantia de Sem Repetição:** Embaralhamento aleatório (shuffle) sem repetir itens dentro da mesma sessão.
- **Cabeçalho Oficial Padronizado:** Mostra `[Banca] - [Ano] - [Órgão/Cargo] | [Assunto]`.

### 4. 📊 Relatórios & Diagnóstico de Desempenho
- Métricas em tempo real gravadas no LocalStorage:
  - Total de questões respondidas e taxa global de acerto (%).
  - Gráfico horizontal interativo com **Recharts** exibindo percentuais por assunto.
  - Tabela detalhada com acertos, erros e rendimento.
- **Diagnóstico Inteligente:**
  - Detecta tópicos com taxa crítica (< 50%) ou em alerta (< 70%).
  - Gera recomendações práticas de revisão pedagógica.
  - Botão de **1 clique** ("Revisar este Conteúdo na Apostila") que direciona automaticamente para o módulo correspondente.

---

## 📐 Schema Obrigatório de Questões (JSON)

Para alimentar ou importar novas questões reais para o sistema:

```json
[
  {
    "id": "IAUPE-2024-CARUARU-PORT-01",
    "banca": "UPENET/IAUPE",
    "grupo_banca": "PE",
    "ano": 2024,
    "orgao": "Prefeitura Municipal de Caruaru - PE",
    "cargo": "Professor de Educação Infantil",
    "assunto": "Crase",
    "texto_associado": "Texto ou excerto de apoio da prova oficial (quando houver)...",
    "enunciado": "Assinale a alternativa em que o uso do sinal indicativo de crase está de acordo com a norma-padrão:",
    "alternativas": [
      { "letra": "A", "texto": "Entregou o projeto à uma comissão técnica." },
      { "letra": "B", "texto": "A professora dirigiu-se à sala de aula dos alunos do infantil." },
      { "letra": "C", "texto": "Ela começou à falar sobre o desenvolvimento das crianças." },
      { "letra": "D", "texto": "Refiro-me à todos os educadores presentes." }
    ],
    "resposta_correta": "B",
    "explicacao_gabarito": "Na alternativa B, ocorre a fusão da preposição 'a' exigida pelo verbo 'dirigiu-se' com o artigo definido feminino 'a' que acompanha o substantivo 'sala'. Nas demais, a crase é proibida antes de artigo indefinido (uma), verbo (falar) e pronome indefinido (todos)."
  }
]
```

---

## 🎨 Design & Recursos Adicionais
- 🌓 **Dark / Light Mode** com alternância instantânea e persistência local.
- 📱 **Totalmente responsivo** (smartphones, tablets e computadores).
- 💾 **Gerenciador de Banco de Questões:** Importação em lote de arquivos JSON com validação de esquema e exportação de backups.
- 🎉 **Animações de conquista** com confetes quando o usuário atinge mais de 70% de acertos nos simulados.
