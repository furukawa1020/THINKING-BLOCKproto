# 🧠 THINKING BLOCKS

**Program your way of thinking.**

THINKING BLOCKS は、思考をプログラムのように構造化し、可視化するためのブロックプログラミング環境です。ScratchやBlocklyのような直感的な操作で、「なぜ」「どのように」「何を」という思考の構造を組み立てることができます。

## ✨ 特徴

- 🧩 **直感的なブロック操作**: ドラッグ&ドロップで思考構造を構築
- 🎨 **5つの思考ブロック**: WHY、HOW、WHAT、OBSERVE、REFLECT
- 📊 **3つの出力形式**: テキスト構文、JSON、マインドマップ
- 🎭 **4つのテーマ**: 創造、内省、研究、教育
- 💾 **保存・共有機能**: ローカル保存とデータ共有
- 🌈 **温かみのあるデザイン**: 瞑想的で親しみやすいUI

## 🎯 ターゲットユーザー

- **思考家・研究者**: 哲学・デザイン・HCI・教育などで"問い"を扱う専門家
- **学習者**: 自己理解・探究学習・論文構想・プレゼン構造化に使う学生  
- **カウンセラー・コーチ**: クライアントの思考を構造化・可視化するツールとして利用
- **クリエイター**: アイデアの動機・意図・構造を整理するために利用

## 🛠️ 技術スタック

- **Frontend**: Next.js 16, React 19, TypeScript
- **Styling**: Tailwind CSS
- **Block Editor**: Google Blockly
- **Icons**: Lucide React
- **Fonts**: Quicksand (Google Fonts)

## 🚀 開発・起動方法

### 前提条件
- Node.js 20.9.0以上

### インストールと起動

```bash
# リポジトリをクローン
git clone https://github.com/furukawa1020/THINKING-BLOCKproto.git
cd thinking-blocks

# 依存関係をインストール
npm install

# 開発サーバー起動
npm run dev
```

ブラウザで [http://localhost:3000](http://localhost:3000) を開いてアプリケーションを確認してください。

## 📝 使い方

1. **ブロックの配置**: 左パネルから思考ブロックをドラッグ&ドロップ
2. **テキスト入力**: 各ブロックに思考内容を入力
3. **構造の確認**: 右パネルで思考構造をテキスト・JSON・マップで確認
4. **保存・共有**: 思考構造を保存したり、他の人と共有

## 🧩 ブロックの種類

| ブロック | 色 | 目的 | 例 |
|---------|---|------|-----|
| **WHY** | 🟡 黄色 | 動機・理由 | "なぜこれをしたいのか？" |
| **HOW** | 🟢 緑色 | 手段・方法 | "どのようにやるのか？" |
| **WHAT** | 🔵 青色 | 目的・成果 | "何を達成するのか？" |
| **OBSERVE** | 🟠 オレンジ | 現状観察 | "現状はどうなっているか？" |
| **REFLECT** | 🟣 紫色 | 振り返り | "どう改善できるか？" |

## 📊 出力形式

### テキスト構文
```
WHY("人の考えを構造化したい")
  HOW("ブロックで可視化する")
    WHAT("思考プログラミング環境をつくる")
OBSERVE("現状：考えが抽象的すぎる")
REFLECT("より直感的な可視化を導入する必要がある")
```

### JSON構造
```json
{
  "thinking_structure": {
    "created_at": "2024-10-31",
    "theme": "creative",
    "blocks": [...]
  }
}
```

### マインドマップ
Canvas技術を使った視覚的な思考マップ表示

## 🎨 テーマ

- **創造** (Creative): 紫〜ピンクのグラデーション
- **内省** (Introspection): 青〜ティールのグラデーション  
- **研究** (Research): 緑〜青のグラデーション
- **教育** (Education): 黄〜オレンジのグラデーション

## 🗂️ プロジェクト構造

```
thinking-blocks/
├── src/
│   ├── app/
│   │   ├── layout.tsx       # ルートレイアウト
│   │   ├── page.tsx         # メインページ
│   │   └── globals.css      # グローバルスタイル
│   └── components/
│       ├── ThinkingBlocksApp.tsx  # メインアプリコンポーネント
│       ├── BlocklyEditor.tsx      # Blocklyエディタ
│       └── OutputViewer.tsx       # 出力表示
├── package.json
└── README.md
```

## 🔮 今後の拡張予定

- [ ] **v1.1**: AIリフレクション（GPT API連携）
- [ ] **v2.0**: ネットワーク共有・共同編集・教育用ライセンス展開  
- [ ] **v3.0**: メタ思考AIエージェント（思考履歴をトレーニング）

## 📄 ライセンス

MIT License

## 🤝 コントリビューション

プルリクエストやイシューの報告をお待ちしています！

---

> "Think like you code." - THINKING BLOCKS