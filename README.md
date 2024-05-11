# Poc-Gemini-Imersao-Alura
## Análise Inteligente de Cupons Fiscais com Google Gemini

Este projeto utiliza o poder do Google Gemini, um modelo de IA multimodal de última geração, para analisar imagens de notas fiscais, extrair dados relevantes, categorizar produtos, detectar anomalias e responder a perguntas sobre a compra.

### Funcionalidades:
- Extração de Dados: Extrai nomes de produtos e preços de imagens de notas fiscais utilizando OCR e processamento de linguagem natural (PNL).
- Correção de OCR: Utiliza o Google Gemini para corrigir erros comuns de OCR, melhorando a precisão dos dados extraídos.
- Categorização de Produtos: Agrupa os produtos em categorias (ex: alimentos, bebidas) utilizando técnicas de clustering.
- Detecção de Anomalias: Identifica compras suspeitas, como preços muito altos, que podem indicar erros ou fraudes.
- Interface de Chatbot: Permite que você faça perguntas sobre a nota fiscal em linguagem natural, como "Quanto gastei com frutas?" ou "Qual o item mais caro da compra?", e o Gemini fornece respostas relevantes.

### Requisitos de Instalação:

Python 3.7 ou superior: https://www.python.org/

Bibliotecas Python:
- pip install pytesseract Pillow spacy scikit-learn google-generativeai
- pytesseract: Realiza OCR (Optical Character Recognition) para extrair texto da imagem da nota fiscal.
- Pillow (PIL): Processa a imagem da nota fiscal.
- spacy: Biblioteca de PNL utilizada para analisar o texto extraído e identificar entidades relevantes.
- scikit-learn: Fornece algoritmos de clustering para categorização de produtos.
- google-generativeai: Biblioteca para interagir com os modelos de IA Generativa do Google AI, incluindo o Gemini.

Tesseract OCR:
- Faça o download e instale o Tesseract OCR: https://github.com/tesseract-ocr/tesseract
- Windows: Adicione o caminho para a pasta tesseract.exe na variável de ambiente PATH.

Modelo de Linguagem do spacy:
-python -m spacy download pt_core_news_sm
Baixa o modelo de linguagem português para o spacy.

Chave de API do Google Cloud:
Crie um projeto no Google Cloud Platform e ative a API Generative AI: https://cloud.google.com/generative-ai
Obtenha sua chave de API e configure-a no código: genai.configure

### Utilização:
 - Crie uma chave chamada genaiKey no colab por exemplo e use o valor da sua chave de API do Google Cloud.
- Execute o script Python.
- O programa solicitará o caminho para a imagem da nota fiscal no seu computador.
- Após processar a imagem, o programa exibirá:
    - Categorias de Produtos
    - Anomalias Detectadas (se houver)
- Em seguida, você poderá interagir com o chatbot, fazendo perguntas sobre a nota fiscal em linguagem natural.
- Digite "sair" para encerrar o programa.

### Observações:
- O Google Gemini é um modelo de IA em desenvolvimento. Sua disponibilidade e funcionalidades podem mudar com o tempo.
- Este projeto é um ponto de partida e pode ser expandido e personalizado para atender às suas necessidades específicas.
