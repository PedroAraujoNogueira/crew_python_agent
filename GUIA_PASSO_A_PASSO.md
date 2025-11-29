# Guia Passo a Passo - Como Rodar o Projeto Python

## 📋 Pré-requisitos

Antes de começar, você precisa ter:
1. **Python 3.8 ou superior** instalado
2. **pip** (gerenciador de pacotes do Python) instalado
3. Chaves de API:
   - **OPENAI_API_KEY** (da OpenAI)
   - **SERPER_API_KEY** (do Serper.dev)

---

## 🚀 Passo a Passo

### Passo 1: Verificar se o Python está instalado

Abra o terminal e digite:
```bash
python3 --version
```

Se não estiver instalado, instale o Python 3.8 ou superior.

### Passo 2: Navegar até a pasta do projeto

No terminal, navegue até a pasta do projeto:
```bash
cd /home/pedro/Documentos/Aquecimento1_gentsAI
```

### Passo 3: Criar um ambiente virtual (recomendado)

Criar um ambiente virtual é uma boa prática para isolar as dependências do projeto:

```bash
python3 -m venv venv
```

Ativar o ambiente virtual:
```bash
source venv/bin/activate
```

Você verá `(venv)` no início da linha do terminal, indicando que o ambiente virtual está ativo.

### Passo 4: Instalar as dependências

Com o ambiente virtual ativado, instale as dependências do projeto:

```bash
pip install -r requirements.txt
```

Isso instalará:
- CrewAI
- langchain
- openai
- python-dotenv

### Passo 5: Criar o arquivo .env

Crie um arquivo chamado `.env` na pasta do projeto com as suas chaves de API:

```bash
nano .env
```

Ou usando qualquer editor de texto. Adicione as seguintes linhas (substitua pelos seus valores reais):

```
OPENAI_API_KEY=sua_chave_openai_aqui
SERPER_API_KEY=sua_chave_serper_aqui
```

**Onde conseguir as chaves:**
- **OPENAI_API_KEY**: https://platform.openai.com/api-keys
- **SERPER_API_KEY**: https://serper.dev/api-key

### Passo 6: Verificar se o arquivo .env foi criado corretamente

Certifique-se de que o arquivo `.env` está na mesma pasta que o `app2.py`:

```bash
ls -la | grep .env
```

### Passo 7: Executar o projeto

Com tudo configurado, execute o projeto:

```bash
python3 app2.py
```

Ou simplesmente:

```bash
python app2.py
```

### Passo 8: Aguardar a execução

O projeto irá:
1. Carregar as variáveis de ambiente
2. Criar 4 agentes (Researcher, Writer, Developer, Reviewer)
3. Executar as tarefas sequencialmente
4. Exibir os resultados

Isso pode levar alguns minutos, pois os agentes fazem pesquisas na internet e geram conteúdo.

---

## 📝 Notas Importantes

1. **Ambiente Virtual**: Sempre ative o ambiente virtual antes de executar o projeto
2. **Chaves de API**: Nunca compartilhe suas chaves de API publicamente
3. **Custos**: O uso da API da OpenAI e Serper pode ter custos associados
4. **Tempo de Execução**: O projeto pode levar alguns minutos para executar completamente

---

## ✅ Verificação Final

Antes de executar, verifique:
- [ ] Python 3.8+ instalado
- [ ] Ambiente virtual criado e ativado
- [ ] Dependências instaladas (`pip install -r requirements.txt`)
- [ ] Arquivo `.env` criado com as chaves de API
- [ ] Está na pasta correta do projeto

---

Boa sorte! 🎉

