# Gemini Document Processor

Este projeto utiliza a API Gemini da Google para processar e recuperar documentos relacionados a procedimentos operacionais padrões em PDF. Desenvolvido durante a semana de imersão da Alura em parceria com a Google, este projeto demonstra a aplicação de inteligência artificial generativa na gestão de documentos de RH.

## Instalação

Para instalar as bibliotecas necessárias, execute o seguinte comando:

```bash
pip install -U -q google-generativeai
```

## Configuração
Antes de começar, é necessário configurar a API Key fornecida pelo Google Colab:

```python
from google.colab import userdata
import google.generativeai as genai

GOOGLE_API_KEY = userdata.get('GOOGLE_API_KEY')
genai.configure(api_key=GOOGLE_API_KEY)
```

## Uso
O projeto já vem com uma série de documentos padrões que podem ser utilizados para teste. Para adicionar ou modificar os documentos, ajuste o conteúdo das variáveis DOCUMENT1, DOCUMENT2, DOCUMENT3, e DOCUMENT4.

Para processar e buscar nos documentos, utilize a função searchInProcess(query, base, model), substituindo query pela sua pergunta específica.

Exemplo de uso:

```python
question = "Como funciona o processo de contratação?"
print(searchInProcess(question, df, model))
```

## Contribuindo
Contribuições são sempre bem-vindas! Veja como você pode contribuir:

Fork o repositório e crie sua branch a partir de main.
Faça suas alterações e teste-as.
Envie um pull request com uma descrição detalhada de suas mudanças.

## Agradecimentos
Agradeço à Alura e à Google pela oportunidade e recursos fornecidos para realizar este projeto.
