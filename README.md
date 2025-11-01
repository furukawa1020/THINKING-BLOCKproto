# 🧠 THINKING BLOCKS

**人間の思考を可視化する革新的なビジュアルプログラミング環境**

思考のプロセスをブロックで構造化し、深い洞察と新しい発見をもたらします。

## ✨ 特徴

### 🎨 フロントエンド (Next.js 16 + React 19)
- **🎯 思考フレームワークブロック**: WHY, HOW, WHAT, OBSERVE, REFLECT, CONNECT
- **🎮 100種類以上のプログラミングブロック**: 
  - イベント処理、制御フロー、変数管理
  - 数値計算、文字列操作、配列・辞書
  - ネットワーク通信、ファイル操作
  - 時間制御、ユーティリティ
- **💎 16カテゴリ**: C/Python/JavaScript/すべての言語の良いところを統合
- **🎨 4つのテーマ**: Creative, Introspection, Research, Education
- **📊 3つの出力形式**: テキスト構文、JSON、マインドマップ
- **🤖 AI思考分析**: パターン検出と改善提案
- **📤 多様なエクスポート**: Markdown, JSON, SVG, PNG
- **⌨️ キーボードショートカット**: Ctrl+S (保存), Ctrl+O (開く), Ctrl+E (エクスポート)
- **🎭 美しい実行結果表示**: 四角い枠とグラデーションヘッダー

### ⚡ バックエンド (Go 1.23)
- **RESTful API**: Gin Webフレームワーク
- **リアルタイム共同編集**: Gorilla WebSocket
- **データ永続化**: PostgreSQL 16 + Redis 7
- **認証・認可**: JWT認証
- **アナリティクス**: 思考パターン分析と統計

### 🐳 インフラ
- **Docker Compose**: フルスタック環境を一発起動
- **マイクロサービス**: フロントエンド、バックエンド、DB、キャッシュ
- **スケーラブル**: 水平スケーリング対応

## 🎮 プログラミングブロック一覧

### 基本カテゴリ
1. **🎯 思考フレームワーク** - 背景哲学としての思考整理
2. **🎮 イベント** - プログラム開始、クリック、キー入力、タイマー、カスタム
3. **🔄 制御フロー** - if/else, for, while, switch-case, try-catch
4. **� 変数とスコープ** - const定数、ポインタ、グローバル変数
5. **🔢 数値・計算** - ビット演算、累乗、平方根、絶対値、丸め処理

### 高度なカテゴリ
6. **📝 文字列操作** - split, replace, substring, format, 正規表現
7. **📋 配列・リスト** - push/pop, slice, map/filter/reduce, sort
8. **🗂️ 辞書・オブジェクト** - dict操作, JSON parse/stringify
9. **⚙️ 関数定義** - 通常関数、ラムダ関数、return文
10. **🎨 出力・表示** - console.log/error/warn, alert, 図形描画

### 実用カテゴリ
11. **📥 入力** - prompt, confirm, ユーザー入力待ち
12. **🌐 ネットワーク・API** - HTTP GET/POST, Fetch API, WebSocket
13. **💾 ファイル・ストレージ** - ファイル読み書き、localStorage
14. **🧮 論理演算** - boolean, 比較演算, 論理演算, 三項演算子
15. **⏱️ 時間・遅延** - sleep, 現在時刻, フォーマット, タイマー
16. **🔧 ユーティリティ** - 型チェック, 型変換, ランダム選択, コメント

## �🚀 クイックスタート

### 方法1: Docker Compose（推奨）

```bash
# リポジトリをクローン
git clone https://github.com/furukawa1020/THINKING-BLOCKproto.git
cd THINKING-BLOCKproto

# 全サービスを起動
docker-compose up --build

# ブラウザで開く
# フロントエンド: http://localhost:3000
# バックエンドAPI: http://localhost:8080
```

### 方法2: ローカル開発

#### 前提条件
- Node.js 20+
- Go 1.23+
- PostgreSQL 16+
- Redis 7+
- Docker (推奨)

#### セットアップスクリプト実行

**Windows (PowerShell):**
```powershell
.\setup.ps1
```

**macOS/Linux:**
```bash
chmod +x setup.sh
./setup.sh
```

#### 手動セットアップ

```bash
# 1. データベース起動
docker-compose up -d postgres redis

# 2. バックエンド起動
cd backend
cp .env.example .env
go mod download
go run main.go  # ポート 8080

# 3. フロントエンド起動（別ターミナル）
cd ..
npm install
npm run dev  # ポート 3000
```

## 📁 プロジェクト構造

```
thinking-blocks/
├── src/                      # Next.jsフロントエンド
│   ├── app/                  # App Router
│   │   ├── api/             # Next.js API Routes (開発用)
│   │   ├── layout.tsx       # ルートレイアウト
│   │   └── page.tsx         # メインページ
│   ├── components/          # Reactコンポーネント
│   │   ├── ThinkingBlocksApp.tsx    # メインアプリ
│   │   ├── BlocklyEditor.tsx        # Blocklyエディタ
│   │   ├── OutputViewer.tsx         # 出力ビューア
│   │   ├── MindMapCanvas.tsx        # マインドマップ
│   │   ├── AIReflection.tsx         # AI分析
│   │   └── ExportService.tsx        # エクスポート
│   ├── hooks/               # カスタムフック
│   │   └── useCollaboration.ts      # リアルタイム共同編集
│   └── lib/                 # ユーティリティ
│       ├── api-client.ts    # APIクライアント
│       └── db.ts            # データベースクライアント
│
├── backend/                 # Goバックエンド
│   ├── main.go             # エントリーポイント
│   ├── config/             # 設定
│   ├── database/           # データベース層
│   │   ├── database.go
│   │   └── models.go
│   ├── api/                # APIハンドラー
│   │   └── handler.go
│   ├── websocket/          # WebSocket
│   │   ├── hub.go
│   │   └── client.go
│   ├── go.mod              # Go依存関係
│   ├── Dockerfile          # Goコンテナ
│   └── .env.example        # 環境変数サンプル
│
├── docker-compose.yml      # Docker設定
├── Dockerfile              # Next.jsコンテナ
├── setup.sh                # Linuxセットアップ
├── setup.ps1               # Windowsセットアップ
├── BACKEND.md              # バックエンドAPI仕様
└── README.md               # このファイル
```

## 🎯 使い方

### 基本的な使い方

#### 1. 思考フレームワークブロック（背景哲学）
思考を整理するための基盤となるブロック:
- **WHY**: なぜ？根本原因を探る
- **HOW**: どうやって？方法・プロセス
- **WHAT**: 何を？具体的な内容
- **OBSERVE**: 観察事実を記録
- **REFLECT**: 振り返りと学び
- **CONNECT**: アイデアを結びつける

#### 2. プログラミングブロック
実際のコードを書くためのブロック（Scratch風）:

**制御フロー:**
```
🎮 プログラム開始時 → 実行
🔄 もし～なら → 条件分岐
🔄 10回繰り返す → ループ
🔄 while条件 → 繰り返し
```

**変数と計算:**
```
📦 変数 x = 10
🔢 x + y
🔢 x × 2
🔢 余り x ÷ 3
```

**文字列操作:**
```
📝 "Hello" + "World"
📝 文字列を分割（区切り文字: ","）
📝 置換（"old" → "new"）
```

**配列・リスト:**
```
📋 配列を作成
📋 配列に追加
📋 配列をソート（昇順/降順）
📋 map/filter/reduce
```

**入出力:**
```
📥 ユーザーから入力
💬 表示する "結果"
📝 console.log
🔔 アラート表示
```

**ネットワーク:**
```
🌐 HTTP GET "https://api.example.com"
🌐 HTTP POST（データ付き）
🔌 WebSocket接続
```

### プログラミング例

#### 例1: 繰り返し処理
```
🎮 プログラム開始時
  📦 変数 count = 0
  🔄 10回繰り返す
    💬 表示する count
    📦 count = count + 1
```

#### 例2: 条件分岐
```
🎮 プログラム開始時
  📥 変数 age = ユーザー入力
  🔄 もし age >= 20 なら
    💬 表示する "成人です"
  🔄 そうでなければ
    💬 表示する "未成年です"
```

#### 例3: 配列操作
```
🎮 プログラム開始時
  📋 配列 numbers = [1, 2, 3, 4, 5]
  📋 配列 doubled = numbers.map(x * 2)
  💬 表示する doubled
```

### テーマを選択
- **Creative**: 創造的思考
- **Introspection**: 内省・自己分析
- **Research**: 研究・調査
- **Education**: 学習・教育

### 出力形式
- **テキスト**: シンプルな構文表示（四角い枠で見やすく）
- **JSON**: データ構造として保存
- **マインドマップ**: ビジュアル表示

### エクスポート
- Markdown, JSON, SVG, PNG形式で保存
- 共有リンク生成
- リアルタイム共同編集

## 🔧 API仕様

詳細は [BACKEND.md](./BACKEND.md) を参照

### 主要エンドポイント

```
GET    /api/v1/projects          - プロジェクト一覧
POST   /api/v1/projects          - プロジェクト作成
GET    /api/v1/projects/:id      - プロジェクト取得
PUT    /api/v1/projects/:id      - プロジェクト更新
DELETE /api/v1/projects/:id      - プロジェクト削除

POST   /api/v1/projects/:id/share - 共有リンク生成
GET    /api/v1/share/:token       - 共有アクセス

POST   /api/v1/ai/analyze         - AI思考分析

WS     /ws/:projectId             - リアルタイム共同編集
```

## 🌐 デプロイ

### Vercel (フロントエンド)
```bash
vercel deploy
```

### Railway/Heroku (バックエンド)
```bash
# Railway
railway init
railway up

# Heroku
heroku create
heroku addons:create heroku-postgresql
heroku addons:create heroku-redis
git push heroku main
```

### Docker
```bash
docker-compose up -d --build
```

## 🛠️ 技術スタック

| カテゴリ | 技術 |
|---------|------|
| **フロントエンド** | Next.js 16, React 19, TypeScript, Tailwind CSS 4 |
| **バックエンド** | Go 1.21, Gin, GORM, Gorilla WebSocket |
| **データベース** | PostgreSQL 16, Redis 7 |
| **インフラ** | Docker, Docker Compose |
| **ビジュアル** | Google Blockly, Canvas API |
| **アイコン** | Lucide React |
| **フォント** | Quicksand (Google Fonts) |

## 📊 パフォーマンス

- **初回ロード**: < 2秒
- **リアルタイム同期**: < 100ms
- **同時接続**: 1000+ユーザー対応
- **データベース**: インデックス最適化済み

詳細は [PERFORMANCE.md](.github/PERFORMANCE.md) を参照してください。

## 🔄 CI/CD

### GitHub Actions パイプライン

[![CI/CD Pipeline](https://github.com/furukawa1020/THINKING-BLOCKproto/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/furukawa1020/THINKING-BLOCKproto/actions/workflows/ci-cd.yml)

- ✅ **自動テスト**: フロントエンド・バックエンド両方
- 🐳 **Dockerビルド**: マルチステージビルド最適化
- 🔒 **セキュリティスキャン**: Trivyによる脆弱性検出
- 📦 **アーティファクト管理**: ビルド成果物の保存
- 🚀 **自動デプロイ**: mainブランチへのプッシュで自動実行（オプション）

### ローカルでCI/CDチェック

**Windows:**
```powershell
.\scripts\ci-check.ps1
```

**macOS/Linux:**
```bash
chmod +x scripts/ci-check.sh
./scripts/ci-check.sh
```

詳細は [CI/CD設定ガイド](.github/CICD.md) を参照してください。

## 🤝 コントリビューション

プルリクエスト大歓迎！

1. フォーク
2. フィーチャーブランチ作成 (`git checkout -b feature/amazing`)
3. コミット (`git commit -m 'Add amazing feature'`)
4. プッシュ (`git push origin feature/amazing`)
5. プルリクエスト作成

## 📝 ライセンス

MIT License

## 🎓 Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Go Documentation](https://golang.org/doc/)
- [Blockly Documentation](https://developers.google.com/blockly)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)

## 👥 作者

Created with ❤️ by furukawa1020

---

**🌟 思考の可視化で、新しい発見を！**
