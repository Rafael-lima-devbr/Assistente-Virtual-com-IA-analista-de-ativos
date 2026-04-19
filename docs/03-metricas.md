# Avaliação e Métricas

## Como Avaliar seu Agente

No estágio atual do projeto, não foi possível realizar uma avaliação prática completa do agente.

Isso ocorreu por dois fatores principais:

Limitação de conhecimento teórico em RAG (Retrieval-Augmented Generation), especialmente na construção de pipelines robustos de recuperação e validação de dados;
Limitações de recursos computacionais, que impediram a execução contínua e testes reais do agente em ambiente local.

Dessa forma, a avaliação foi conduzida apenas em nível conceitual, com base no comportamento esperado do sistema.
---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | Se o agente responde corretamente com base nos dados coletados | Esperado: respostas baseadas em dados reais (preço, notícias, indicadores) |
| **Segurança** | Se evita invenção de informações (alucinação) | Esperado: declarar ausência de dados quando necessário |
| **Coerência** | Se a resposta é lógica e alinhada ao contexto financeiro | Esperado: recomendações consistentes com os dados analisados |

---

## Exemplos de Cenários de Teste

### Teste 1: Consulta de gastos
- **Pergunta:** "VALE3 vale a pena?"
- **Resposta esperada:** Análise estruturada baseada em dados (preço, histórico, notícias e indicadores), com recomendação, riscos e limitações
- **Resultado:** Não foi possível avaliar na prática

### Teste 2: Recomendação de produto
- **Pergunta:** "Qual investimento você recomenda para mim?"
- **Resposta esperada:** Recomendação compatível com o perfil do usuário ou solicitação de mais informações caso o perfil não esteja definido
- **Resultado:** Não foi possível avaliar na prática
  
### Teste 3: Pergunta fora do escopo
- **Pergunta:** "Qual a previsão do tempo?"
- **Resposta esperada:** Agente informa que só trata de análise financeira
- **Resultado:** Não foi possível avaliar na prática

### Teste 4: Informação inexistente
- **Pergunta:** "Analise um ativo sem dados disponíveis"
- **Resposta esperada:** Agente declara ausência de dados suficientes e não faz recomendação
- **Resultado:** Não foi possível avaliar na prática

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**
Estrutura do agente orientada a dados (uso de ferramentas externas como base)\
Separação clara entre coleta de informações e geração de análise\
Definição de regras para evitar respostas inventadas\
Organização da resposta em formato estruturado (recomendação, riscos, fontes e limitações)

**O que pode melhorar:**
Execução prática do agente para validação real dos resultados\
Maior aprofundamento teórico em RAG (Retrieval-Augmented Generation)\
Implementação de testes com usuários reais\
Melhor adaptação do sistema para rodar em ambientes com menor capacidade computacional

---

## Métricas Avançadas (Opcional)

Para quem quer explorar mais, algumas métricas técnicas de observabilidade também podem fazer parte da sua solução, como:

- Latência e tempo de resposta;
- Consumo de tokens e custos;
- Logs e taxa de erros.

Ferramentas especializadas em LLMs, como [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/), são exemplos que podem ajudar nesse monitoramento. Entretanto, fique à vontade para usar qualquer outra que você já conheça!
