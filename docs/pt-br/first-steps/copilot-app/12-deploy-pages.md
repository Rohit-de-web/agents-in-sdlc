---
title: "Lição 12: publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o fluxo de trabalho e orientar a publicação, mas você é responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a publicação no GitHub Pages.
- revisar o fluxo de trabalho e o pull request antes de fazer o merge.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma maneira simples de experimentá-lo. Publicar o site de arquivo único com o GitHub Pages o disponibiliza em uma URL pública sem adicionar um servidor nem uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de três etapas: um pull request de space-quiz mesclado; uma execução bem-sucedida de Deploy website no GitHub Actions com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede que o agente crie e faça merge de um pull request e altere as configurações do Pages no repositório. Antes de continuar, revise o diff, as permissões de publicação e todas as solicitações de aprovação do GitHub.

## Revise o fluxo de trabalho e verifique a publicação

1. Confirme que o README só foi adicionado se ainda não existia no repositório.
2. Revise as alterações do pull request, incluindo as etapas de build e publicação do fluxo de trabalho.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de publicação do GitHub Actions até que ela seja concluída.
5. Acesse a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou fazer o merge do pull request, siga as instruções específicas fornecidas por ele. Não considere a tarefa concluída até que a publicação seja bem-sucedida e o site esteja disponível.

## Resumo e próximas etapas

O Space Quiz agora está disponível como um site, e você verificou a publicação em vez de confiar apenas no relato do agente. Continue para a [Lição 13: revisão e próximas etapas][next-lesson].

[next-lesson]: ../13-review/
