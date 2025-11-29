# Guia: Configurar Git e Fazer Push para Repositório Remoto

## 📋 Pré-requisitos

1. Ter um repositório Git criado no GitHub, GitLab, Bitbucket ou outro serviço
2. Ter o Git instalado no seu sistema
3. Ter as credenciais de acesso ao repositório remoto

---

## 🚀 Passo a Passo

### Passo 1: Verificar o status atual do Git

```bash
cd /home/pedro/Documentos/Aquecimento1_gentsAI
git status
```

### Passo 2: Adicionar todos os arquivos ao staging

```bash
git add .
```

Isso adiciona todos os arquivos ao staging (exceto os que estão no `.gitignore`).

### Passo 3: Fazer o primeiro commit

```bash
git commit -m "Initial commit: projeto CrewAI com agentes de pesquisa"
```

Ou use uma mensagem mais descritiva:

```bash
git commit -m "feat: adiciona projeto CrewAI com agentes de pesquisa, escrita, desenvolvimento e revisão"
```

### Passo 4: Adicionar o repositório remoto

Substitua `SEU_USUARIO` e `SEU_REPOSITORIO` pelos valores reais:

**Para GitHub:**
```bash
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
```

**Para GitLab:**
```bash
git remote add origin https://gitlab.com/SEU_USUARIO/SEU_REPOSITORIO.git
```

**Para Bitbucket:**
```bash
git remote add origin https://bitbucket.org/SEU_USUARIO/SEU_REPOSITORIO.git
```

**Exemplo real:**
```bash
git remote add origin https://github.com/pedro/aquecimento1-gentsai.git
```

### Passo 5: Verificar se o remote foi adicionado corretamente

```bash
git remote -v
```

Você deve ver algo como:
```
origin  https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git (fetch)
origin  https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git (push)
```

### Passo 6: Renomear o branch principal (opcional, mas recomendado)

Se o repositório remoto usa `main` ao invés de `master`:

```bash
git branch -M main
```

### Passo 7: Fazer o push para o repositório remoto

**Primeira vez (push inicial):**
```bash
git push -u origin main
```

Ou se estiver usando `master`:
```bash
git push -u origin master
```

O flag `-u` (ou `--set-upstream`) configura o branch para rastrear o remoto, então nas próximas vezes você pode usar apenas:
```bash
git push
```

---

## 🔧 Comandos Úteis Adicionais

### Verificar o remote atual
```bash
git remote -v
```

### Alterar a URL do remote (se necessário)
```bash
git remote set-url origin https://github.com/SEU_USUARIO/NOVO_REPOSITORIO.git
```

### Remover um remote
```bash
git remote remove origin
```

### Ver todos os branches
```bash
git branch -a
```

### Ver o histórico de commits
```bash
git log --oneline
```

---

## 🔐 Autenticação

### Usando HTTPS (recomendado para iniciantes)

1. **GitHub**: Você precisará de um Personal Access Token (PAT)
   - Vá em: Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Crie um novo token com permissões de `repo`
   - Use o token como senha quando o Git pedir

2. **GitLab**: Similar ao GitHub, use um Personal Access Token

### Usando SSH (mais seguro, mas requer configuração)

1. Gere uma chave SSH:
```bash
ssh-keygen -t ed25519 -C "seu_email@exemplo.com"
```

2. Adicione a chave pública ao seu perfil no GitHub/GitLab

3. Use a URL SSH ao adicionar o remote:
```bash
git remote add origin git@github.com:SEU_USUARIO/SEU_REPOSITORIO.git
```

---

## ⚠️ Solução de Problemas

### Erro: "remote origin already exists"
Se você já tem um remote configurado e quer alterá-lo:
```bash
git remote set-url origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
```

### Erro: "failed to push some refs"
Se o repositório remoto já tem commits que você não tem localmente:
```bash
git pull origin main --allow-unrelated-histories
git push -u origin main
```

### Erro de autenticação
- Verifique se você está usando o token correto (HTTPS)
- Ou verifique se sua chave SSH está configurada (SSH)

### Verificar configuração do Git
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu_email@exemplo.com"
```

---

## 📝 Checklist Rápido

- [ ] Repositório Git inicializado (`git init` - já feito)
- [ ] Arquivos adicionados ao staging (`git add .`)
- [ ] Primeiro commit criado (`git commit -m "mensagem"`)
- [ ] Remote adicionado (`git remote add origin URL`)
- [ ] Push realizado (`git push -u origin main`)

---

## 🎯 Exemplo Completo (Copie e Cole)

```bash
# 1. Navegar até a pasta do projeto
cd /home/pedro/Documentos/Aquecimento1_gentsAI

# 2. Adicionar arquivos
git add .

# 3. Fazer commit
git commit -m "feat: projeto inicial CrewAI com agentes de pesquisa"

# 4. Adicionar remote (SUBSTITUA pela URL do seu repositório)
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git

# 5. Renomear branch para main (se necessário)
git branch -M main

# 6. Fazer push
git push -u origin main
```

---

Boa sorte! 🚀

