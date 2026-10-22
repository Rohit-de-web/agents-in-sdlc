---
title: "レッスン 12: GitHub Pages でサイトをデプロイする"
description: "GitHub Copilot アプリを使って Pages のワークフローを構成し、プルリクエストを確認して、公開された Space Quiz を検証します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Space Quiz を GitHub Pages にデプロイして、誰でもアクセスできるようにします。Copilot はワークフローの準備とデプロイの案内を行えますが、変更を確認し、サイトが公開されたことを検証するのはユーザーの役割です。

このレッスンでは、次のことを行います。

- GitHub Pages のデプロイを構成するよう Copilot に依頼します。
- マージする前に、ワークフローとプルリクエストを確認します。
- デプロイの状況を追跡し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、試してもらうには簡単な方法が必要です。GitHub Pages を使って単一ファイルのサイトを公開すると、サーバーやランタイム依存関係を追加せずに、公開 URL からアクセスできるようになります。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot アプリのセッションで、次のプロンプトを送信します。

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![3 段階の図: マージ済みの space-quiz プルリクエスト、Build website、Upload artifact、Deploy to Pages の各ステップを含む GitHub Actions の Deploy website 成功実行、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトは、エージェントにプルリクエストの作成とマージ、およびリポジトリの Pages 設定の変更を依頼します。続行する前に、差分、デプロイ権限、GitHub の承認要求を確認してください。

## ワークフローを確認してデプロイを検証する

1. リポジトリに README がない場合に限り、README が追加されていることを確認します。
2. ワークフローのビルドとデプロイの手順を含め、プルリクエストの変更を確認します。
3. 必須のプルリクエストチェックが成功した後にのみマージします。
4. GitHub Actions のデプロイ実行を追跡し、成功するまで確認します。
5. 報告された URL を開き、Space Quiz が読み込まれることを確認します。

エージェントが Pages を有効にできない場合やプルリクエストをマージできない場合は、エージェントが示す具体的な手順に従います。デプロイが成功し、公開サイトが読み込まれるまで、作業を完了したと見なさないでください。

## まとめと次のステップ

Space Quiz が公開され、エージェントの報告に頼らずにデプロイを検証できました。[レッスン 13: レビューと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
