# Codexでの導入確認

2026-10-06 / Linux / Codex CLI 0.154.0

## 確認済み

- 対象はコミット `42dd126` の `skills/narke`。
- Codex付属のskill-installerでGitHubから取得できた。
- 作業フォルダへの配置後、`diff -r` で元のSkillフォルダと一致した。
- `SKILL.md` と `references/perspectives.md`、`references/question-map.md`、`references/report.md` が含まれる。

## 未完了と理由

ユーザー共通の配置先への書き込み許可を取得したが、この実行環境では `~/.codex/skills` と `~/.agents` への書き込みが `Read-only file system` で失敗した。グローバルインストール完了とは扱わない。

CodexによるSkillの自動検出、`$narke` での起動、複数ターンの対話、理解度レポートは未検証。READMEの操作例は利用例であり、実行結果ではない。

## 実環境での確認手順

1. READMEの手順でユーザー共通のSkillフォルダに配置する。
2. 次のターンで `$narke` と `tests/fixtures/sample-proposal.md` を指定する。認識されなければCodexを再起動する。
3. 始めの約束、引用付きの問い、1回最大10問を確認する。
4. 正しい説明、誤り、「わからない」を回答し、途中で正誤を示さず問いを深めることを確認する。
5. 「ここまで」と送り、回答ごとの評価と、資料の欠陥を区別した未解決一覧を確認する。
6. 保存を頼む前にレポートがファイル保存されないことを確認する。論点台帳の作業ファイルは別扱いとする。

共通の確認項目は [scenarios.md](scenarios.md) にある。そこでのClaude Codeの結果をCodexの検証結果として扱わない。
