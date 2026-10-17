# Micro SaaS 企画テンプレート

Micro SaaS の企画から公開までを、ドキュメント駆動で進めるためのテンプレート。
AI エージェント（Claude Code など）と一緒に進めることを前提にしている。

## 構成

| ファイル | 役割 |
|---|---|
| [docs/project.md](docs/project.md) | 企画書（誰の何を解決するか、MVP の範囲、価格、集客） |
| [docs/validation.md](docs/validation.md) | 課題検証の記録（ヒアリング、仮説の成否） |
| [docs/decisions.md](docs/decisions.md) | 事業・方針レベルの意思決定ログ |
| [docs/pricing.md](docs/pricing.md) | 価格設定、コスト、損益分岐 |
| [docs/legal/](docs/legal/) | 利用規約・プライバシーポリシー・特商法表記の雛形（公開前に要確認） |
| [docs/launch-checklist.md](docs/launch-checklist.md) | 公開前チェックリスト |
| [ROADMAP.md](ROADMAP.md) | マイルストーンと進捗 |
| [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/) | バグ報告・機能要望の Issue テンプレート |
| [docs/design/_template.md](docs/design/_template.md) | 設計書のテンプレート |
| [AGENTS.md](AGENTS.md) | AI エージェント向けのルール（`CLAUDE.md` から読み込まれる） |
| [.env.example](.env.example) | 必要な環境変数の一覧 |

## 使い方

1. このリポジトリをコピーして新しいプロジェクトを作る
   - GitHub の「Use this template」、またはクローンして `.git` を消して `git init`
2. [docs/project.md](docs/project.md) を埋める。例文は消して自分の内容に置き換える
3. [docs/validation.md](docs/validation.md) に、ターゲットへのヒアリングを記録する。**作り始める前に需要を確かめる**
4. [ROADMAP.md](ROADMAP.md) の〔 〕を埋め、ゴールと目標日を決める
5. 設計が必要な作業ごとに、`docs/design/_template.md` をコピーして `docs/design/NN-名前.md` を作る
6. 技術スタックが決まったら、[AGENTS.md](AGENTS.md) の「技術スタック」「コマンド」を埋める
7. `.env.example` を `.env` にコピーして値を入れる（`.env` はコミットしない）

## 進め方

- 作業の起点は ROADMAP。完了したら `[x]` にする
- 🚧（作業中）は同時に1つ
- 👤 が付いた項目は、コード以外の人の作業（ヒアリング、申請、告知など）
- 設計書の「決定事項」は上書きしない。変更は取り消し線と理由で残す

## 書き換えの目印

〔 〕で囲んだ部分は、プロジェクトごとに書き換える箇所。
すべて埋めたら、この README もそのプロジェクト用の内容に差し替える。
