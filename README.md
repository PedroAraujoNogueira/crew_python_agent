# Sistema de Agentes de IA usando CrewAI e LangChain

### Como executar o projeto:

-> Crie um ambiente virtual Python (recomendado):
```bash
python3 -m venv venv
source venv/bin/activate  # No Linux/Mac
# ou
venv\Scripts\activate  # No Windows
```

-> Instale as dependências do projeto:
```bash
pip install -r requirements.txt
```

-> Adicione as variáveis de ambiente abaixo no arquivo `.env` na raiz do projeto:

```
OPENAI_API_KEY=SUA_CHAVE_OPENAI
SERPER_API_KEY=SUA_CHAVE_SERPER
```

-> Execute o projeto:
```bash
python app2.py
```

### Descrição do projeto:

O projeto é uma aplicação de IA feita usando CrewAI e LangChain, utilizando os serviços da OpenAI e Serper API. Nesse projeto criamos uma equipe de agentes especializados que trabalham em conjunto para criar um tutorial completo sobre agentes de IA.

A equipe é composta por:
- **Researcher (Pesquisador)**: Responsável por pesquisar informações sobre agentes de IA e bibliotecas como LangChain usando a ferramenta de busca na internet.
- **Writer (Escritor)**: Desenvolve a estrutura e conteúdo do tutorial de forma didática.
- **Developer (Desenvolvedor)**: Fornece exemplos práticos de código para implementação de agentes.
- **Reviewer (Revisor)**: Revisa o conteúdo final garantindo clareza e precisão.

O workflow utiliza o processo sequencial, onde cada agente executa sua tarefa em ordem, e um modelo GPT-4o-mini atua como gerente para coordenar o trabalho da equipe.

O objetivo desse projeto foi aprender sobre criação de agentes de IA colaborativos usando CrewAI e como integrar ferramentas customizadas (como busca na internet) para expandir as capacidades dos agentes.

### Requisitos de software e bibliotecas:

-> Python 3.8 ou superior

-> CrewAI

-> LangChain e LangChain-OpenAI

-> OpenAI API

-> Serper API (para busca na internet)

-> python-dotenv (para gerenciamento de variáveis de ambiente)

-> requests (para requisições HTTP)

### Estrutura do projeto:

```
crew_python_agent/
├── app2.py                 # Arquivo principal com a definição dos agentes e workflow
├── Tools/
│   └── search_tools.py     # Ferramenta customizada de busca na internet
├── requirements.txt        # Dependências do projeto
├── .env                    # Arquivo de variáveis de ambiente (criar manualmente)
└── README.md              # Este arquivo
```

### Links úteis:

Documentação CrewAI: https://docs.crewai.com/

Documentação LangChain: https://python.langchain.com/

OpenAI API: https://platform.openai.com/

Serper API: https://serper.dev/
