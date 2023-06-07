# Gerador de Powerpoint

Este script Python, chamado `main.py`, usa várias bibliotecas para criar uma apresentação de slides Powerpoint (.pptx) a partir de documentos PDF. Ele faz isso utilizando o modelo de linguagem GPT da OpenAI e a API de imagens da OpenAI para gerar imagens.

O script lê documentos PDF e, usando o modelo GPT, transforma esse conteúdo em um conjunto de slides no formato JSON. Em seguida, ele cria um arquivo de apresentação Powerpoint (.pptx) para cada documento, com cada slide contendo um título, conteúdo e uma imagem conceitual gerada a partir da API de imagens da OpenAI.

## Pacotes Necessários
Os pacotes Python necessários para executar este script são:
- pandas
- pyarrow
- llama-index
- gpt-index
- openai
- pypdf
- python-dotenv
- typer
- python-pptx
- requests

## Variáveis de Ambiente
O script requer a seguinte variável de ambiente:

- `OPENAI_API_KEY`: A chave de API para o serviço OpenAI. Esta chave é necessária para acessar os modelos de linguagem e a API de imagens da OpenAI.

## Configurando o Ambiente
Para executar este script Python, siga as seguintes etapas:

1. Instale os pacotes necessários usando o arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

2. Configure a variável de ambiente. Crie um arquivo `.env` no diretório do script e adicione sua chave de API para a OpenAI:

```bash
echo "OPENAI_API_KEY=<sua chave da OpenAI>" >> .env
```

Lembre-se de substituir `<sua chave da OpenAI>` pela sua chave real.

3. Execute o script com os parâmetros necessários:

```bash
python main.py <diretorio_de_pdfs> --output_folder <diretorio_de_saida> --index_folder <diretorio_temporario>
```

Substitua `<diretorio_de_pdfs>`, `<diretorio_de_saida>` e `<diretorio_temporario>` pelos seus diretórios reais.

## Notas

- As pastas de saída e temporária serão criadas automaticamente pelo script se elas não existirem.
- Se o diretório temporário já existir, todos os arquivos nele serão apagados antes de começar a processar os novos documentos.
- Todos os documentos PDF no diretório de pdfs serão processados.
- A chave da OpenAI é necessária para a execução do script, não esqueça de configurar a variável de ambiente corretamente.