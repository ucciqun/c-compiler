# c-compiler
簡単なcコンパイラです

## test.shに書かれたテストを実行する
```
docker build -t compilerbook https://www.sigbus.info/compilerbook/Dockerfile
docker run --rm -v $HOME/cc:/cc -w /cc compilerbook make test
```

## Git運用について
### コミットメッセージの規則を以下に統一します
- `fix`：バグ修正
- `hotfix`：クリティカルなバグ修正
- `add`：新規（ファイル）機能追加
- `update`：機能修正（バグではない）
- `change`：仕様変更
- `clean`：整理（リファクタリング等）
- `disable`：無効化（コメントアウト等）
- `remove`：削除（ファイル）
- `upgrade`：バージョンアップ
- `revert`：変更取り消し
