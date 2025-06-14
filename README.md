# 251-sint-grupo26
🌐 Projeto Flask com Integração API Gemini
Pitão Frasco API Gemini Status

Este é um projeto web desenvolvido com Flask que oferece ofertas educativas e interativas sobre Python, com glossário, conteúdo explicativo e integração com a API Gemini (Google AI) para respostas inteligentes.

📁 Estrutura do Projeto
python-infos/

├── app.py # Aplicação Flask principal

├── requisitos.txt # Dependências do projeto

├── .env # Configurações sensíveis (não versionado)

├── bd_glossario.csv # Banco de dados de termos

└── modelos/

├── modelo.html # Layout base

├── index.html # Página inicial

├── gemini.html # Interface do assistente AI

├── glossario.html # Lista de termos

├── novo_termo.html # Formulário de adição

└── ... # Demais páginas

📚 Seções
Página Inicial ( /) : Apresentação do site.
Glossário ( /glossario) : Lista de termos e significados sobre programação.
Conteúdo ( /conteudo) : Explicações desenvolvidas sobre Python.
Quiz ( /quiz) : Avaliação dos conhecimentos adquiridos.
🚀 Tecnologias Utilizadas
Python 3.10+
Flask (framework web)
SDK de IA generativa do Google ( google.generativeai)
dotenv para carregar variáveis ​​de ambiente
HTML + Bootstrap para modelos
🤖 Integração com API Gemini
A integração não está no arquivo app.py:

genai.configure(api_key=os.getenv("API_KEY"))

def call_gemini_api(prompt):
    model = genai.GenerativeModel("gemini-2.0-flash")
    response = model.generate_content(prompt)
    return response.text
🧩 Principais Partes do Código
app.py: Controle de rotas e lógica principal.

call_gemini_api(): Chama a API Gemini com um prompt.

carregar_glossario(): Leia o CSV de termos.

templates/: Contém páginas renderizadas com Flask (Jinja2).

bd_glossario.csv: Base local do glossário (termo;significado).

🚀 Como Executar
Clonar ou repositório

Configurar o ambiente:

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
pip install -r requirements.txt
Crie um arquivo .env:

GENAI_API_KEY=sua_chave
FLASK_SECRET_KEY=chave_secreta
Início ou servidor:

flask run
👥 Colaboradores
Paulo César Eduardo Cabral Vitor Rodrigo João Vitor
