# 損害保険 評価研修用 3Dビューア (Agricultural & Building Insurance Assessment 3D Viewers)

農業共済(NOSAI)の**園芸施設共済**および**建物共済**の評価研修を想定した、ブラウザで動くインタラクティブな3Dモデル集です。Three.js製・単一HTMLファイルで、インターネット接続があればダブルクリックで起動できます(インストール不要)。

> **技術メモ:** Three.js は最新安定版(0.184.0, r184)を ES Modules + importmap 方式で CDN から読み込みます。

**🔗 デモ: https://<GitHubユーザー名>.github.io/<リポジトリ名>/**
*(公開後、実際のURLに書き換えてください)*

## 収録ビューア

| ファイル | 内容 |
|---|---|
| [`viewers/engei-kyosai-3d-viewer.html`](viewers/engei-kyosai-3d-viewer.html) | 園芸施設共済向け。プラスチックハウスⅡ類(パイプハウス)・Ⅳ類(鉄骨屋根型)・Ⅵ類(雨よけ施設)・Ⅶ類(多目的ネットハウス)・ガラス室Ⅱ類の5型式を切替表示。施設構造部分(妻面/側面/屋根面/基礎、Ⅶ類は周囲面/天井面/基礎)の色分け表示、被覆材切替、部材マーカー付き。 |
| [`viewers/tatemono-kyosai-3d-viewer.html`](viewers/tatemono-kyosai-3d-viewer.html) | 建物共済向け。木造在来工法の一般住宅を平屋/2階建てで切替。軸組(柱・梁・筋かい・小屋組等)・外装(屋根材/外壁材はテクスチャ切替)・内装(床・天井・間仕切り・階段)を再現し、部位色分け・骨組み表示・内部透過表示に対応。 |

## 特徴

- 単一HTMLファイル(依存はThree.js CDNのみ) — ダウンロードしてダブルクリックするだけで起動
- ドラッグで回転、ホイール/ピンチでズーム
- 部材・部位ごとにマーカーを配置し、タップで評価上の着眼点を表示
- 型式・階数・屋根材/外壁材/被覆材の切替に対応

## 使い方

### そのまま開く
`viewers/` 内のHTMLファイルをダウンロードし、ブラウザで開くだけで動作します(インターネット接続が必要です。Three.jsをCDNから読み込むためです)。

### ローカルで動かす
```bash
git clone https://github.com/<GitHubユーザー名>/<リポジトリ名>.git
cd <リポジトリ名>
# お好みのブラウザで viewers/*.html を直接開いてください
```

## ⚠️ 免責事項(必ずお読みください)

- 本リポジトリのモデルは**研修・学習用の簡略化されたイメージ**であり、農林水産省「園芸施設共済評価要領」や各農業共済組合の正式な損害評価基準・様式を完全に再現したものではありません。
- 園芸施設共済ビューアの型式・部材・数値は、公開されている評価要領(平成30年5月2日 30経営第367号、以下 改正含む)の記載内容を参考にしていますが、寸法・部材構成は表示用に簡略化・縮小しています。
- 建物共済ビューアの部位区分・着眼点の解説は、一般的な木造建築の部位名称と公開情報に基づく研修用の参考であり、NOSAIの正式な部位区分表・損害割合基準を再現したものではありません。
- 実際の引受評価・損害評価・支払可否の判断は、必ず各農業共済組合等の公式な評価要領・約款・基準に基づいて行ってください。本ツールの内容と齟齬がある場合は公式資料が優先します。

## ライセンス

Apache License 2.0 のもとで公開しています。詳細は [LICENSE](LICENSE) を参照してください。

```
Copyright [year] [your name]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

`[year]` と `[your name]` は公開時にご自身の情報に置き換えてください。

## 貢献

Issue・Pull Requestを歓迎します。特に以下は歓迎です。

- 未収録の型式(連棟式、Ⅰ類・Ⅲ類・Ⅴ類など)の追加
- 実際の評価様式・部位区分表に基づく精緻化(該当資料をお持ちの方からのフィードバック歓迎)
- UI/UXの改善、多言語対応
