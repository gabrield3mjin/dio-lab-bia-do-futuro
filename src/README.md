# Passo a Passo de Execução

## Setup do Ollama

```bash
# 1. Instalar o Ollama (ollama.com)
# 2. Baixar um modelo leve OU rodar um modelo via nuvem (RECOMENDADO! - modelos exigem muito da memória RAM para rodar localmente)
ollama pull gpt-oss (comando no cmd caso opte por baixar o modelo localmente)
```

## Código Completo

Todo o código-fonte está no arquivo `app.py`

## Como Rodar

```bash
# 1. Instalar dependências
pip install streamlit pandas requests

# 2. Garantir que o Ollama está rodando
ollama serve

# 3. Rodar a aplicação
streamlit run .\src\app.py
```
