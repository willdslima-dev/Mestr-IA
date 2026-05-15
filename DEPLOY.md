# 🚀 GUIA RÁPIDO - Deploy GitHub Pages

## ✅ Pasta Prod Pronta!

**Tamanho:** 1.4 MB | **Arquivos:** 9

```
Prod/
├── .nojekyll              ← Necessário para GitHub Pages
├── index.html             ← Página principal
├── asset-manifest.json    ← Manifesto de assets
├── README.md              ← Documentação
└── static/
    ├── css/               ← Estilos (8.21 KB gzip)
    │   └── main.c470f997.css
    └── js/                ← JavaScript (88 KB gzip)
        └── main.58dbccaf.js
```

---

## 📋 Passo a Passo - Subir para GitHub

### 1️⃣ Inicializar Git na pasta Prod

```bash
cd C:\GitNeon\Local\Mestre.Ia\Prod
git init
git add .
git commit -m "Deploy inicial - DevCom v1.0"
```

### 2️⃣ Conectar ao GitHub

**Opção A - Novo Repositório:**
```bash
# Criar repositório no GitHub primeiro, depois:
git remote add origin https://github.com/SEU-USUARIO/devcom-app.git
git branch -M main
git push -u origin main
```

**Opção B - Repositório Existente (branch específica):**
```bash
git remote add origin https://github.com/SEU-USUARIO/seu-repo.git
git checkout -b gh-pages
git push -u origin gh-pages
```

### 3️⃣ Ativar GitHub Pages

1. Acesse: `https://github.com/SEU-USUARIO/seu-repo/settings/pages`
2. Em **Source**:
   - Branch: `main` (ou `gh-pages`)
   - Folder: `/ (root)`
3. Clique **Save**
4. Aguarde ~2 minutos

### 4️⃣ Acessar App

URL: `https://SEU-USUARIO.github.io/seu-repo/`

---

## ⚙️ Configurar IA no App Online

1. Acesse o app online
2. Clique no ícone **⚙️ Configurações**
3. Acesse **Painel de IA**
4. Cole sua chave do Google Gemini
5. Teste a conexão
6. Pronto! IA funcionando

**Obs:** A chave fica salva apenas no seu navegador (localStorage)

---

## 🔄 Atualizar Deploy (Futuras Versões)

```bash
# Na pasta DevCom-Ia, gerar novo build:
npm run build

# Copiar para Prod:
cd C:\GitNeon\Local\Mestre.Ia
Remove-Item "Prod\static" -Recurse -Force
Copy-Item "DevCom-Ia\build\*" -Destination "Prod\" -Recurse -Force

# Fazer commit e push:
cd Prod
git add .
git commit -m "Atualização v1.x"
git push
```

---

## ✨ Funcionalidades do App

- ✅ Gestão de pedidos e orçamentos
- ✅ Cadastro de clientes
- ✅ IA para linguagem natural (opcional)
- ✅ Agenda e calendário
- ✅ Geração de documentos
- ✅ Modo local (funciona sem IA)
- ✅ Tema claro/escuro
- ✅ Dados salvos no navegador

---

**Build:** 15/05/2026
**Versão:** 1.0.0
