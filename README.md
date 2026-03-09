# Teste de Sincronização - Documentação

Repositório de teste para a GitHub Action `tooling-sync-gh-docs`.

Este repositório demonstra como usar a action para sincronizar automaticamente documentação com Google Docs quando um PR é mergeado.

## 📁 Estrutura

```
teste-documentacao/
├── docs/
│   └── prds/              # Pasta monitorada pela action
│       ├── prd-001.md
│       └── prd-002.md
├── .github/
│   └── workflows/
│       └── sync-docs.yml   # Workflow que dispara a action
└── README.md
```

## 🚀 Como usar

### 1. Configurar Secrets

No repositório, adicione os seguintes secrets em **Settings → Secrets and variables → Actions**:

- `GOOGLE_SERVICE_ACCOUNT`: JSON da Service Account do Google
- `GOOGLE_DOC_ID`: ID do documento Google onde sincronizar

### 2. Fazer uma mudança na pasta `docs/prds/`

Edite ou crie um arquivo em `docs/prds/`::

```bash
git checkout -b feature/update-prd-001
# Edite docs/prds/prd-001.md
git add docs/prds/prd-001.md
git commit -m "Update PRD 001"
git push origin feature/update-prd-001
```

### 3. Criar e Mergear um Pull Request

1. Abra um PR no GitHub
2. Mergear o PR
3. A action será executada automaticamente
4. O conteúdo será sincronizado com o Google Doc configurado

## 📝 Arquivos de Exemplo

Este repositório inclui alguns arquivos de exemplo em `docs/prds/`:

- **prd-001.md**: Exemplo de PRD (Documento de Requisitos de Produto)
- **prd-002.md**: Outro exemplo de PRD

Você pode editá-los ou criar novos arquivos conforme necessário.

## ✅ Verificar se funcionou

Após fazer merge de um PR:

1. Vá para a aba **Actions** no GitHub
2. Procure pelo workflow **Sync docs on PR merge**
3. Clique no último run para ver os logs
4. Se bem-sucedido, você deve ver a mensagem:
   ```
   ✓ Google Doc updated successfully
   ```

## 🔗 Referências

- [Action no GitHub](https://github.com/vtex/tooling-sync-gh-docs)
- [Documentação completa](https://github.com/vtex/tooling-sync-gh-docs/blob/main/README.md)

## 🤔 Dúvidas?

Consulte a seção de **Troubleshooting** na documentação da action ou abra uma issue.
