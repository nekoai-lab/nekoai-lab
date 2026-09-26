# nekoai-lab

<!-- このリポジトリのルールの正本。AGENTS.md（Codex 用）はここを指すだけ -->

## 概要

nekoai-lab の GitHub プロフィール README（public）。プロフィールに表示されるのは README.md だけ。コードの開発対象ではない（REPOS.md のレーン「—」）。

## よく使うコマンド

| 用途 | コマンド |
|---|---|
| install | `（未定）` |
| dev | `（未定）` |
| lint | `（未定）` |
| test | `（未定）` |
| build | `（未定）` |

## レーン

`—`（正本は `tasks/current.md` の1行目。基準は `~/Projects/ai-dev-harness/policies/lanes.md`）

## 共通ルール

作業の前に `~/Projects/ai-dev-harness/bin/preflight` を実行し、`~/Projects/ai-dev-harness/policies/` を読むこと。

- git-flow.md：ブランチ → PR → CI・レビュー → テストが通れば AI がマージ
- agents.md：役割、1 Issue = 1 Agent = 1 Branch = 1 Worktree（`~/Projects/nekoai-lab.wt/<branch>/`）、交代の順番
- lanes.md：full / solo
- secrets.md：鍵の値は表示しない。`.env*` は .gitignore

## 完了の定義

- [ ] build・lint・test が通る
- [ ] `tasks/current.md` を更新した（現状／やり残し／次の1手）
- [ ] PR を作り、CI が通った
- [ ] full は、実装者と別の AI のレビューでラベル `qa-pass`（UI の変更ありは `ux-pass` も）が付いた。付かないうちはマージしない

## このリポジトリ固有のルール

- README.md は **main に直接編集してよい**（`.github/direct-push-allow`。GitHub の画面からの編集を含む）。上の「完了の定義」は README の直接編集には当てはめない
- それ以外（`.github/`・この CLAUDE.md・AGENTS.md・`tasks/`・`.gitignore`）はブランチ → PR
- public なので、コミットは noreply アドレス（REPOS.md の置き場所のルール）
