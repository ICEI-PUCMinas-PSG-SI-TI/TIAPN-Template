# 6. Métricas
Guia de Qualidade e Boas Práticas na Modelagem BPMN

Para garantir que os diagramas **TO-BE** desenvolvidos pela equipe sejam claros, legíveis e sirvam de base sólida para a criação do Banco de Dados e dos Requisitos (Seção 4), o modelo de vocês será avaliado com base em critérios de **Complexidade Estrutural e Clareza**. 

Vocês não precisam calcular fórmulas matemáticas complexas, mas devem seguir as diretrizes abaixo para evitar modelos confusos ou sobrecarregados:

---

## 7.1. Métricas de Complexidade Estrutural no BPMN

As métricas de complexidade ajudam a identificar se um processo está muito intrincado, o que aumenta a taxa de erros e dificulta a compreensão pelo restante da equipe:

* 📏 **Tamanho do Modelo (*Size*):** Refere-se à contagem total de elementos do diagrama (atividades, gateways, eventos e fluxos de sequência). 
  * *Boa prática:* Evite diagramas gigantescos. Se um processo tiver mais de 30 a 40 elementos visuais, considere quebrá-lo em **subprocessos** para manter a legibilidade.
* 🔗 **Densidade e Acoplamento (*Coupling*):** Mede o grau de interconexão entre as tarefas e os dados do processo. 
  * *Boa prática:* Evite que uma única tarefa converse diretamente com muitas outras de forma desorganizada. O fluxo deve seguir uma lógica sequencial e natural de negócio.
* 🔀 **Complexidade de Controle (*Control-flow Complexity*):** Avalia a quantidade de desvios lógicos baseados em *gateways* (XOR, AND, OR). 
  * *Boa prática:* Cuidado com o excesso de ramificações paralelas e cruzamentos de linhas. Todo *gateway* de abertura (paralelo ou exclusivo) deve ter um fechamento claro correspondente para evitar fluxos órfãos.

---

## 7.2. Checklist de Validação do Modelo TO-BE

Antes de finalizar a modelagem BPMN, verifique se o diagrama da equipe atende aos seguintes pontos:

- [ ] **Legibilidade Visual:** O diagrama possui o mínimo cruzamento possível de linhas de fluxo (*sequence flows*)?
- [ ] **Padronização de Nomes:** Todas as atividades começam com um verbo no infinitivo (ex: *Cadastrar Cliente*, *Validar Pagamento*)?
- [ ] **Eventos de Início e Fim:** O processo possui claramente um Evento de Início e pelo menos um Evento de Fim definidos?
- [ ] **Alinhamento com o Sistema:** As atividades mapeadas nos fluxos cobrem exatamente as funcionalidades que virarão Requisitos Funcionais (RF) nas próximas etapas?
