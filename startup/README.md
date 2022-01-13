# startup

チュートリアルを実行
[はじめに \| Vite](https://ja.vitejs.dev/guide/#vite-%E3%82%92%E3%82%AA%E3%83%B3%E3%83%A9%E3%82%A4%E3%83%B3%E3%81%A7%E8%A9%A6%E3%81%99)

## やってみる

### viteのプロジェクト作成

コマンドを実行すると、プロジェクト名の設定と、いくつかのテンプレートから一つ選ぶ、今回は他との違いを知るため vanilla

```bash
npm init vite@latest
# or
# npm init vite@latest startup -- --template vanilla

cd startup
npm install
npm run dev
```

- note: この時点で、vite用のconfigファイルは無い

#### テンプレート違いによるconfig構成の違い

vanilla-ts, svelte-tsの場合 以下のようになった

- vanilla-ts: tsconfig.jsonが追加される
  - srcディレクトリが作成されその中にmain.tsが追加
- svelte-ts: tsconfjg.json, vite.config.js, svelte.config.js が追加される
  - srcディレクトリ内にmain.ts及びsvelteファイルが追加

特に、viteでtypescript用の設定などは行わない。ドキュメントにあるようにisolation

### viteのコマンド

package.jsonには以下の用に記載される。なんとなくコマンドの意味合いがわかる。
他のコマンドは `npx vite --help` で確認可能

buildは、トランスパイルされたファイルがdistフォルダに出力される

```json
{
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
}
```
