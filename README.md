# kaikit-jp.github.io

KAIKIT の公式サイト。GitHub Pages で `https://kaikit-jp.github.io/` に公開する。

## 中身

| ファイル | 公開URL | 用途 |
| --- | --- | --- |
| `index.html` | `https://kaikit-jp.github.io/` | トップページ。Play Console の「デベロッパーのWebサイト」に登録する |
| `privacy/kakimo/index.html` | `https://kaikit-jp.github.io/privacy/kakimo/` | カキモのプライバシーポリシー。Play Console に登録する |
| `app-ads.txt` | `https://kaikit-jp.github.io/app-ads.txt` | AdMob の収益を守る宣言ファイル。**必ずルート直下** |
| `.nojekyll` | — | GitHub Pages の Jekyll 処理を止め、置いたファイルをそのまま配信させる |

## 公開のしかた

1. GitHub で **`kaikit-jp`** というアカウント（または Organization）を用意する
2. そのアカウントに **`kaikit-jp.github.io`** という名前のリポジトリを作る（Public）
3. このフォルダの中身をそのまま push する

   ```bash
   git init
   git add .
   git commit -m "KAIKIT のサイトを公開"
   git branch -M main
   git remote add origin https://github.com/kaikit-jp/kaikit-jp.github.io.git
   git push -u origin main
   ```

4. リポジトリの **Settings → Pages** で、Source が `Deploy from a branch` / `main` / `/ (root)` になっていることを確認する
5. 数分待って `https://kaikit-jp.github.io/` が開けたら完了

リポジトリ名が `kaikit-jp.github.io` ちょうどでないと、URL に
`/リポジトリ名/` が挟まって app-ads.txt がルート直下にならない。

## app-ads.txt について

```
google.com, pub-7810187821133921, DIRECT, f08c47fec0942fa0
```

AdMob 管理画面 → アプリ → **app-ads.txt** に表示される行と一致しているか、
公開後に必ず見比べること。行が違うと認識されない。

反映の手順:

1. Play Console のストア掲載情報で「デベロッパーのWebサイト」を
   `https://kaikit-jp.github.io/` にする
2. AdMob 管理画面で「確認」を押す
3. 反映まで最大24時間ほどかかる

Play Console に登録したドメインと、app-ads.txt を置いたドメインが
一致していないと AdMob が見つけられない。

## プライバシーポリシーを直すとき

`privacy/kakimo/index.html` を編集する。日本語と英語の両方が1ページに入っている。
内容を変えたら、ページ上部の日付（`制定日` / `Effective date`）も更新する。
