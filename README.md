# c-compiler
簡単なcコンパイラです

https://www.sigbus.info/compilerbook#%E7%B0%A1%E5%8D%98%E3%81%AA%E4%BE%8B


## 使い方
`test.sh`に記述するか、`cc`ディレクトリで以下の通りに実行する。
```
cc -o cc cc.c
./cc "[コンパイルしたい文字列かファイル]" >tmp.s
cc -o tmp tmp.s
.tmp
echo $?
```

## test.shに書かれたテストを実行する
`test.sh`に
```
assert [予期した結果] [コンパイルしたい文字列]
```
を追加した後で、
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
