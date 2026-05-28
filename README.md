# Enjoy Med · Plano de Ação Operacional

Página web do plano de ação operacional da **Enjoy Med**, consolidado a partir da reunião de **27/05**. Reúne as **11 ações** com responsáveis, prazos, prioridades e status, em três visões interativas e com filtros.

**Site publicado:** https://enjoy-cowork.github.io/enjoy-med-site/

---

## O que tem na página

- **11 ações** detalhadas (instrução objetiva + critério de pronto), expandíveis ao clicar.
- **3 visões:**
  - **Lista** — todos os cards, com detalhes expansíveis.
  - **Kanban** — agrupado por status (A iniciar · Em andamento · Bloqueado · Concluído).
  - **Por Responsável** — ações agrupadas por dono direto.
- **Filtros e busca:** por frente, responsável, prazo, prioridade, status e texto livre.
- **Identidade visual Enjoy:** navy `#0D1F3C` + gold `#C9A84C`, fonte **Montserrat**.
- 100% estático (HTML/CSS/JS em arquivo único). Sem dependências de build.

## Estrutura

```
.
├── index.html                  # a página (tudo em um arquivo)
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml          # deploy automático no GitHub Pages
```

## Como publicar

O workflow em `.github/workflows/deploy.yml` publica automaticamente a cada push na branch `main`.

1. Crie o repositório `enjoy-med-site` na conta/organização `enjoy-cowork`.
2. Suba estes arquivos na branch `main`:
   ```bash
   git init
   git add .
   git commit -m "Plano de ação operacional Enjoy Med (reunião 27/05)"
   git branch -M main
   git remote add origin https://github.com/enjoy-cowork/enjoy-med-site.git
   git push -u origin main
   ```
3. No GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. O site fica disponível em **https://enjoy-cowork.github.io/enjoy-med-site/** em ~1 minuto.

## Como atualizar o conteúdo

Os dados das ações ficam no array `ACTIONS` dentro de `index.html`. Edite o array, faça commit e push — o deploy roda sozinho.

---

*Base: reunião Enjoy Med de 27/05 · Identidade Enjoy (navy + gold).*
