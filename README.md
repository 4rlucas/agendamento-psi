# Cuidar é Amar — Agendamento

Plataforma interna de agendamento da clínica. Documentação completa em `docs/` — mantida só localmente (não vai para o repositório público).

## Estrutura

```
index.html        → painel Admin/Recepção   (servido em  /)
psicologo.html    → painel do Psicólogo     (servido em  /psicologo.html)
docs/             → documentação (só local, ignorada pelo git)
  prompts/        → prompts usados com agentes de IA
.vercelignore     → impede que docs/ e afins sejam publicados
```

**Deploy:** GitHub → Vercel, site estático sem build. Os dois HTML **precisam ficar na raiz**:
a Vercel os serve pelo caminho do arquivo. Não há `vercel.json` (não é necessário).

Previstos, ainda fora deste diretório: `sql/` (scripts `schema_*.sql`, ver docs/BANCO.md, local)
e `supabase/functions/` (Edge Functions `google-calendar` e `criar-usuario`).
