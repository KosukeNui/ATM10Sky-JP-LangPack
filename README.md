# ATM10 To the Sky 日本語化パック

Minecraft 1.21.1（NeoForge）用のモッドパック **[All the Mods 10: To the Sky](https://www.curseforge.com/minecraft/modpacks/all-the-mods-10-sky)**（ATM10 To the Sky、v2.3.1 対応）の日本語化パックです。

- MOD のアイテム名・画面・説明など 232 名前空間・約35,000キーの翻訳（リソースパック）
- FTB Quests のクエスト（全55章・6,417キー。章の名前・クエストの本文・報酬の説明を含む）
- ガイドブック（リソースパック）
  - Applied Energistics 2 本体とアドオン（AdvancedAE・ExtendedAE・MEGA Cells・AE2WTLib・Applied Flux・ExpandedAE・ME Requester・AE2 Import Export Card・Ars Énergistique）
  - Immersive Engineering のマニュアル（114項目）
  - Excessive Utilities と Oritech の Wiki（Oracle Index）
  - Extreme Reactors・Just Dire Things・LaserIO・Productive Bees・Productive Trees・Modular Bees・RFTools・Railcraft・Building Gadgets 2・Apotheosis（抜けていたページ）など Patchouli の本
  - Happy Hallows・Herbs & Harvest の手引書、Logistics Networks・Little Big Redstone・Extended Industrialization のガイド
  - Neo Vitae・ForceCraft・Actually Additions など、本文を lang で持つ本は本体のリソースパックで日本語になります
- パックのスクリプト（KubeJS）が出すツールチップ・JEI の説明・Silent Gear の独自トレイト・島の選択画面の説明（変換ツール）

シングルプレイでの実機確認をしています。

## ダウンロード

最新版は [Releases](../../releases) からダウンロードしてください。

| ファイル | 中身 |
|---|---|
| `ATM10Sky-JP-1.0.0.zip` | 本体のリソースパック（MOD の翻訳） |
| `ATM10Sky-JP-guidebooks-1.0.0.zip` | ガイドブックのリソースパック |
| `ATM10Sky-JP-Config-1.0.0.zip` | クエストの翻訳（`config/ftbquests/quests/lang/ja_jp.snbt`） |
| `ATM10Sky-JP-converter-1.0.0.html` | 変換ツール（ブラウザで開いて使います） |

## 導入方法（概要）

1. 2つのリソースパックの zip を、解凍せずにインスタンスの `resourcepacks/` フォルダに入れます。
2. `ATM10Sky-JP-Config-1.0.0.zip` を、インスタンスのフォルダ（`config` フォルダと同じ階層）で展開します。
3. 変換ツール（html）をブラウザで開き、インスタンスのフォルダを選んで、変換したファイルをインスタンスに上書きします。
4. ゲームを起動し、**タイトル画面で**2つのリソースパックを有効にして、いちばん上（最優先）に置きます。言語を「日本語」にします。**そのあとで**ワールドに入ります。

くわしくは [インストール手順.txt](./インストール手順.txt) を見てください。

### 変換ツールについて

ATM10 To the Sky は無断転載禁止（All Rights Reserved）のパックなので、パックのファイルを書き換えたものは配布していません。かわりに、**自分のパソコンにあるパックのファイルを書き換える変換ツール**を配布しています。

- 書き換えるのは、画面に出る英語の文を「翻訳キー＋元の英語」の形にする部分だけです。スクリプトの動きや設定の値は変えません。
- 元の英語は残るので、リソースパックを入れていない人や英語の設定の人には、今までと同じ英語が出ます。
- 変換ツールはパソコンの中だけで動き、ファイルをどこにも送信しません。
- パックを更新したら、更新後のファイルでもう一度変換してください。

### マルチプレイの場合

- リソースパックは、参加する人がそれぞれ自分のパソコンに入れます。
- クエストの翻訳（`ja_jp.snbt`）は**サーバーの config に置きます**。FTB Quests はサーバーからクエストの文を送るためです。
- 変換ツールで書き換えるファイルのうち、`config/skyblockbuilder/templates.json5` と `kubejs/data/` の中はサーバーが、`kubejs/client_scripts/` の中は各自のパソコンが読みます。サーバーと各自のパソコンの両方で変換してください。

## 既知の制限事項

- **Oracle Index の Wiki（Excessive Utilities・Oritech）の検索結果は英語で出ます。** 検索の結果は英語の元のページの見出しを使う作りのため、リソースパックでは直せません。検索から開いたページは日本語で出ます。
- **Oritech の Wiki「原子炉の設計の考え方」の表は、ゲームの中に出ません。** 元のページで、ゲームの中では表示されない形（HTML のかたまり）で書かれているためです。英語でも出ません。
- **AE2 のガイドの「アドオン：Ars Énergistique」のページは中身が空です。** MOD の元のページが「...」だけのためです。
- **Apotheosis の本は MOD の公式訳を使っています。** 抜けていたページと、文が古いと確かめたページは訳し足しましたが、ほかのページにも今の版より古い文が残っている可能性があります。
- ガイドブックのリソースパックは、Immersive Engineering のマニュアルの折り返しのために、ふだん使われない空白文字（U+200A）の幅を0にするフォントの設定（`assets/minecraft/font/include/space.json`）を含みます。

## うまく反映されないときは

- JEI の説明やガイドブックの本文などは、**ワールドに入るときに一度だけ**読み込まれます。ワールドに入ってからリソースパックを切り替えると、前の言語のまま残ります。リソースパックはタイトル画面で切り替えてから、ワールドに入り直してください。
- 2つのリソースパックが、ほかのリソースパックより上（優先）にあるか確かめてください。

## フォルダ構成

```
├── resourcepack/   … リソースパック（本体・ガイドブック）
├── config/         … クエストの翻訳（zip）
├── converter/      … 変換ツール（html）
├── translations/   … 本体のリソースパックの訳（名前空間ごとの ja_jp.json。日本語だけ）
├── glossary/       … 訳語集（yaml）
└── インストール手順.txt
```

## 誤訳の報告

誤訳や英語のまま残っている箇所を見つけたら、[Issues](../../issues) で教えてください。どの画面のどの文かと、スクリーンショットがあると助かります。

## ライセンス・注意事項

このリポジトリには日本語の訳だけを含みます。ATM10 To the Sky と、収録されている MOD のファイル・英語の文は含みません。導入には、正規の手段で ATM10 To the Sky を入手してください。
