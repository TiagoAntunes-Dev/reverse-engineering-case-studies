# [App] [Feature] – Case Study

> Estudo de caso: como funciona **[feature]** no **[app]**, investigado com [REA](https://github.com/morluto/rea) (análise estática), com evidências, limitações e a minha própria reimplementação.

## A ideia

Aprendo melhor olhando como apps reais resolvem problemas reais. Neste repo eu escolho **uma feature** de um app que uso, investigo como ela funciona **sem ter o código-fonte** e depois escrevo a minha própria versão.

O foco não é copiar código. É praticar o raciocínio investigativo:

1. Fazer uma pergunta clara.
2. Buscar evidências.
3. Separar o que foi **observado** do que foi **inferido**.
4. Aplicar o que aprendi em um projeto meu.

## Pergunta investigada

> Como funciona [feature] no [app]? Por exemplo: como a busca no Obsidian indexa e filtra as notas?

## Como investiguei

- **Ferramenta:** [REA](https://github.com/morluto/rea), um servidor MCP que conecta o agente de IA a ferramentas de análise de apps.
- **Agente:** [Claude Code / Cursor / Codex]
- **Alvo:** [app + versão], analisado localmente (app Electron/JavaScript).
- **Comando usado:**

```bash
npx -y rea-agents@latest analyze-javascript-application /caminho/do/app --json > evidencia.json
```

## Evidências

Resumo do que o REA retornou (módulos, imports, rotas, IPC) e onde cada achado foi encontrado.

| Achado | Onde foi encontrado | Tipo |
|--------|---------------------|------|
| [ex.: a busca roda em um worker separado] | [módulo/arquivo] | Observado |
| [ex.: o índice é reconstruído a cada abertura] | [módulo/arquivo] | Inferido |

## O que não consegui confirmar

- [ponto 1]
- [ponto 2]

## Minha implementação

Versão própria da feature, escrita do zero com base no que aprendi.

- **Stack:** [ex.: TypeScript, React, Node.js]
- **Pasta:** [`/implementacao`](./implementacao)
- **Como rodar:**

```bash
cd implementacao
npm install
npm start
```

## Estrutura do repo

```
.
├── README.md
├── evidencias/        # resultados do REA (resumos, não o arquivo bruto gigante)
├── notas/             # anotações da investigação
└── implementacao/     # minha versão da feature
```

## Aviso de uso

Este estudo tem fins **educacionais**. Analisei apenas software que uso legalmente, sem burlar licenças e sem redistribuir código do app original. Todo o código em `/implementacao` é de minha autoria.

## Ferramentas e créditos

- [REA – Reverse Engineer Anything](https://github.com/morluto/rea) (licença MIT)
- [App analisado] pertence aos seus respectivos autores.

## Autor

**Tiago Antunes Paz de Oliveira**
[GitHub](https://github.com/TiagoAntunes-Dev) · [LinkedIn](https://linkedin.com/in/tiago-antunes-paz-de-oliveira-174687254)
