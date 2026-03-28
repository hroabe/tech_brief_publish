<!--
---
title: "Tech News Radio — 2026-03-12"
subtitle: "WebAssemblyをWebにおける第一級言語にする / JavaScriptの時間処理を修正するための9年間の旅：Temporal / 間引き処理：サ..."
date: "2026-03-12"
vol: 6
topics:
  - Web
  - OSS
  - Science
  - AI
  - LLM
author: "Hiroki Abe"
---
-->
# 🎧 Tech News Radio — 2026-03-12

> 📖 読了時間: 約11分 ｜ 🏷️ Web, OSS, Science, AI, LLM

---

## 📌 今日のハイライト
- 🌐 **WebAssemblyをWebにおける第一級言語にする** — WebAssemblyをWebのファーストクラス言語へ昇格させる動き
- 🌐 **JavaScriptの時間処理を修正するための9年間の旅：Temporal** — JavaScriptの日時処理をTemporalが9年かけて刷新
- 🔬 **間引き処理：サブリスト証明とde Bruijnインデックスのシフトまとめ** — 型理論における「間引き（Thinning）」の構造的考察
- 🤖 **LLMは進歩が止まったのか？** — LLMはテスト通過率が高くてもコード品質は別問題
- 🌐 **2026年にRailsへの回帰** — 2026年にRailsへ回帰する動きが注目を集める

---

## 🌐 WebAssemblyをWebにおける第一級言語にする
`Web` `OSS`

<details>
<summary>📄 原題: Making WebAssembly a first-class language on the Web</summary>
</details>

> **一言で**: WebAssemblyをWebのファーストクラス言語へ昇格させる動き

- 要点1: WebAssembly（ブラウザ上で動く高速な低レベル実行形式）を、Webのファーストクラス言語として扱う取り組みが進んでいる
- 要点2: 現状ではJavaScriptの補助的な存在にとどまるWebAssemblyを、単独で主役として使えるようにする方向性と見られる
- 要点3: Web標準としての地位向上により、より多様な言語からWebアプリを直接構築できるようになる可能性がある

💡 **なぜ重要か**
WebAssemblyは登場以来、JavaScriptでは難しい高速な数値計算や既存コードの移植に使われてきました。しかし、DOM操作やWeb APIへのアクセスには依然としてJavaScriptが必要で、あくまで補助的な役割に甘んじていました。これをWebの正式な第一級市民として扱うべきだという議論が高まっています。 WebAssemblyがファーストクラスの地位を得れば、RustやC++、Go などで書いたコードがJavaScriptなしで直接Webで動く未来が近づきます。フロントエンド開発の言語選択が広がり、既存のエコシステムやツールチェーンに大きな変化をもたらすと見られます。

🎯 **今日のアクション**
WebAssembly Component ModelやWASI（WebAssembly System Interface）など、関連仕様の最新動向を追いましょう。自社プロダクトでWebAssemblyの活用余地がないか、今のうちに検討しておくと先手を打てます。

🔗 [原文を読む](https://hacks.mozilla.org/2026/02/making-webassembly-a-first-class-language-on-the-web/)

---

## 🌐 JavaScriptの時間処理を修正するための9年間の旅：Temporal
`Web` `OSS`

<details>
<summary>📄 原題: Temporal: The 9-year journey to fix time in JavaScript</summary>
</details>

> **一言で**: JavaScriptの日時処理をTemporalが9年かけて刷新

- 要点1: JavaScriptのDateオブジェクトは30年以上抱えてきた設計上の欠陥がある
- 要点2: 新API「Temporal」はタイムゾーンや暦の扱いを根本から再設計
- 要点3: BloombergがTC39（JavaScript標準化委員会）での策定を9年間主導
- 要点4: 提案は現在Stage 3に到達し、主要ブラウザへの実装が近づいている

💡 **なぜ重要か**
JavaScriptのDateオブジェクトは1995年にJavaから移植された設計をほぼそのまま引き継いでいます。タイムゾーンの扱いが不正確で、月が0始まりだったり、イミュータブル（変更不可）でなかったりと、長年エンジニアの悩みの種でした。そのため現場ではmoment.jsやday.jsといったサードパーティ製ライブラリに頼るのが常識となっていましたが、Temporalはこれをネイティブで解決しようという試みです。 Temporalが標準化されれば、日時処理のためにサードパーティ製ライブラリを導入する必要がなくなります。バンドルサイズ（配信ファイルの容量）削減やパフォーマンス向上につながるほか、日時バグによるインシデントも減ると期待できます。長期的にはJavaScriptエコシステム全体の信頼性底上げに寄与するでしょう。

🎯 **今日のアクション**
まずMDNやTC39のTemporalドキュメントで新APIの設計思想を把握しましょう。polyfill（互換実装ライブラリ）がすでに公開されているため、既存プロジェクトで試験的に使って感覚をつかんでおくと、正式リリース後の移行がスムーズになります。

🔗 [原文を読む](https://bloomberg.github.io/js-blog/post/temporal/)

---

## 🔬 間引き処理：サブリスト証明とde Bruijnインデックスのシフトまとめ
`Science` `OSS`

<details>
<summary>📄 原題: Thinnings: Sublist Witnesses and de Bruijn Index Shift Clumping</summary>
</details>

> **一言で**: 型理論における「間引き（Thinning）」の構造的考察

- 要点1: タイトルが示すのは、型理論・証明支援系に関する学術的な技術記事
- 要点2: 「Sublist Witness（部分リストの証拠項）」と「de Bruijn Index（変数を番号で表す手法）」が主題
- 要点3: スニペットはJavaScriptとMathJaxの設定コードのみで、本文の内容は確認できず

💡 **なぜ重要か**
de Bruijn Indexは、ラムダ計算や型理論で変数名の代わりに数値を使う古典的な手法です。証明支援系（AgdaやCoqなど）の実装では、コンテキストの「間引き（Thinning）」操作が頻出します。この記事はその最適化や構造的性質を論じているとみられます。 証明支援系や依存型言語の実装品質に直結するテーマです。インデックスシフトの効率化は、大規模な形式検証ツールのパフォーマンス改善につながる可能性があります。ただし、スニペットから本文内容を確認できないため、詳細な影響は不明です。

🎯 **今日のアクション**
AgdaやCoqなど証明支援系に携わるエンジニアは、原文を直接参照して詳細を確認することをお勧めします。スニペットにコンテンツがなく、要約は限定的です。

🔗 [原文を読む](https://www.philipzucker.com/thin1/)

---

## 🤖 LLMは進歩が止まったのか？
`AI` `LLM` `DevOps`

<details>
<summary>📄 原題: Are LLMs not getting better?</summary>
</details>

> **一言で**: LLMはテスト通過率が高くてもコード品質は別問題

- METRの調査: LLMのコードは「テスト通過」と「マージ承認」で成功率が大きく乖離
- ベンチマーク（性能指標）の改善が、実用品質の向上を意味しない可能性を示唆
- LLMの「進化」は測定方法に依存しており、評価指標の選び方が本質的に重要

💡 **なぜ重要か**
LLMのコーディング能力はベンチマーク上では向上し続けています。しかし今回の考察は、そのスコアが実際の開発現場で求められる品質と乖離している点を問題提起しています。テストを通過するコードと、レビュアーが承認できるコードは別物であり、評価基準の設計がAIの「賢さ」の見え方を左右します。 AIコーディング支援ツールへの過信が広がる中、ベンチマークを基にした能力評価の信頼性が問われます。開発現場では「テストが通る」だけでなく「保守できるコードか」という視点での検証が不可欠になります。ツールベンダーの主張する性能改善を額面通りに受け取れない時代が来ているとも言えます。

🎯 **今日のアクション**
LLMが生成したコードをレビューする際は、テスト通過だけを合格基準にしないことが重要です。可読性・保守性・設計一貫性を含む独自のレビューチェックリストを用意し、AIツールの採用判断にはベンチマーク以外の実務評価も組み込むべきです。

🔗 [原文を読む](https://entropicthoughts.com/no-swe-bench-improvement)

---

## 🌐 2026年にRailsへの回帰
`Web` `OSS`

<details>
<summary>📄 原題: Returning to Rails in 2026</summary>
</details>

> **一言で**: 2026年にRailsへ回帰する動きが注目を集める

- 要点1: 著者がRuby on Railsへの回帰を2026年時点で改めて語る内容と見られる
- 要点2: かつてRailsから離れた開発者が再評価する流れが背景にある可能性
- 要点3: モダンなWeb開発の複雑化への反動として、Railsの生産性が再注目されているとみられる

💡 **なぜ重要か**
Ruby on Railsは2000年代に一世を風靡しましたが、Node.jsやReactなどの台頭で一時的に影が薄くなりました。しかし近年、開発の複雑さへの疲弊から「シンプルで生産性の高いフレームワーク」を再評価する動きが出ています。この記事はそうした流れを個人の視点で語るものと見られます。 フロントエンドとバックエンドの分離による複雑さが増す中、フルスタックフレームワークの価値が見直されています。RailsのようなMVC（モデル・ビュー・コントローラー）ベースの設計が、特にスモールチームや個人開発者の間で再び選ばれる可能性があります。

🎯 **今日のアクション**
既存のNode.jsやNext.jsベースのプロジェクトと比較して、Railsの開発速度やコスト効率を改めて検証してみましょう。特に小規模チームでは、技術スタックの見直しが生産性向上につながるかもしれません。

🔗 [原文を読む](https://www.markround.com/blog/2026/03/05/returning-to-rails-in-2026/)

---

## 🤖 AIボットに就職面接をされた
`AI` `Business`

<details>
<summary>📄 原題: I was interviewed by an AI bot for a job</summary>
</details>

> **一言で**: AIボットが求職者を面接する時代が到来

- 要点1: 求人選考にAIが面接官として登場し、実際に体験した事例が報告された
- 要点2: 採用プロセスの自動化が進み、人間の採用担当者が不在のまま選考が進む可能性がある
- 要点3: 求職者側はAI面接官への対応という新たなスキルを求められる時代になりつつある

💡 **なぜ重要か**
生成AIの普及により、採用現場でもAIの活用が急速に広がっています。コスト削減や効率化を目的に、初期スクリーニングや面接をAIに任せる企業が増えています。一方で、AIによる選考は公平性やバイアスの問題も抱えており、労働市場への影響は無視できません。 採用担当者の役割が変わり、人事職そのものが再定義される可能性があります。また、求職者はAIに評価されることへの心理的な適応も求められます。長期的には、採用の透明性や説明責任をどう担保するかが業界全体の課題になるでしょう。

🎯 **今日のアクション**
エンジニアやリーダーは、自社の採用フローにAIを導入する際のガイドラインを整備しておくべきです。特にバイアス検証の仕組みと、AI面接の結果を人間が最終確認するプロセスの設計が急務です。

🔗 [原文を読む](https://www.theverge.com/featured-video/892850/i-was-interviewed-by-an-ai-bot-for-a-job)

---

## 🔗 出典一覧
- [WebAssemblyをWebにおける第一級言語にする](https://hacks.mozilla.org/2026/02/making-webassembly-a-first-class-language-on-the-web/)
- [JavaScriptの時間処理を修正するための9年間の旅：Temporal](https://bloomberg.github.io/js-blog/post/temporal/)
- [間引き処理：サブリスト証明とde Bruijnインデックスのシフトまとめ](https://www.philipzucker.com/thin1/)
- [LLMは進歩が止まったのか？](https://entropicthoughts.com/no-swe-bench-improvement)
- [2026年にRailsへの回帰](https://www.markround.com/blog/2026/03/05/returning-to-rails-in-2026/)
- [AIボットに就職面接をされた](https://www.theverge.com/featured-video/892850/i-was-interviewed-by-an-ai-bot-for-a-job)