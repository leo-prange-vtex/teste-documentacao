# Quickstart - Usar a Action neste Repositorio

## 1. Pre-Requisitos

- Google Cloud Project com Docs API habilitada
- Service Account criada com chave JSON
- Google Doc criado e compartilhado com a Service Account
- ID do Google Doc copiado

## 2. Configurar Secrets

1. Va para Settings → Secrets and variables → Actions
2. Clique em New repository secret
3. Crie dois secrets:

### Secret 1: GOOGLE_SERVICE_ACCOUNT
```
Name: GOOGLE_SERVICE_ACCOUNT
Secret: [Cole o conteudo completo do arquivo JSON da Service Account]
```

### Secret 2: GOOGLE_DOC_ID
```
Name: GOOGLE_DOC_ID
Secret: [Cole o ID do documento Google]
```

## 3. Testar a Action

Edite um arquivo em docs/prds/, faca commit, push e crie um PR.

Apos fazer merge do PR, o workflow sera acionado automaticamente.

Va para Actions para verificar se foi bem-sucedido.

## 4. Verificar a Execucao

1. Va para a aba Actions
2. Procure pelo workflow "Sync docs on PR merge"
3. Clique no run mais recente
4. Verifique se passou ou falhou

## Troubleshooting

Consulte QUICKSTART_DETAILED.md para informacoes mais detalhadas.
