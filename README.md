# 🤖 Dário - Assistente Financeiro Inteligente

Dário (**D**iagnóstico e **A**nálise de **R**eserva com **I**nteligência **O**timizada) é um agente inteligente desenvolvido para auxiliar jovens profissionais na organização de suas rendas mensais. O foco central do agente é garantir a manutenção de uma reserva de emergência de 20%, protegendo-a contra gastos excessivos.

---

## 💡 Funcionalidades Principais

* **Organização Salarial**: Divide a renda em três categorias fixas: Custos Fixos, Gastos Livres e Reserva de Emergência.
* **Gestão de Reserva**: Aplica a regra de ouro onde a reserva (padrão de 20% da renda, que pode ser alterado) é subtraída antes de qualquer cálculo de lazer.
* **Lógica Consultiva**: Calcula limites dinâmicos para gastos livres utilizando a fórmula: `Renda - (Custos Fixos + Reserva)`.
* **Reconhecimento de Padrões**: Classifica despesas automaticamente com base em uma base de conhecimento predefinida.
* **Protocolo de Emergência**: Orienta o uso consciente da reserva em casos de emergências reais e planeja sua recomposição.

---

## 🛠️ Arquitetura e Tecnologia

O projeto utiliza uma arquitetura RAG (*Retrieval-Augmented Generation*) para garantir respostas precisas e seguras.

| Componente | Tecnologia |
| --- | --- |
| **Interface** | Streamlit |
| **Cérebro (LLM)** | Ollama (modelo gpt-oss) |
| **Processamento** | Pandas & JSON para injeção de contexto |
| **Base de Dados** | Estrutura mockada em CSV/JSON na pasta `/data` |

---

## 📂 Estrutura de Dados

O agente baseia-se nos seguintes arquivos para suas análises:

* `perfil_cliente.json`: Dados demográficos e metas do usuário.
* `config_usuario.json`: Salário líquido e percentual de reserva alvo.
* `transacoes.csv`: Histórico bruto de entradas e saídas.
* `categorias_padrao.json`: Mapeamento de descrições para categorias.
* `historico_reserva.csv`: Evolução mensal da poupança.
* `historico_atendimento.csv`: Contextualização de interações passadas.

---

## 🚀 Como Executar

As instruções de execução estão no README da pasta `/src`, onde também se encontra a aplicação.

```



---

## 🛡️ Segurança e Qualidade

Dário foi configurado com diretrizes rigorosas contra alucinações: não inventa transações, não acessa senhas e admite quando não possui dados suficientes para um diagnóstico. O sistema foi validado com testes de assertividade e coerência, garantindo que o limite de gastos livres seja sempre respeitado.
