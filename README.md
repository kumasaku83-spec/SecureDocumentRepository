# SDR - Secure Document Repository

> A secure, zero-server document repository that keeps your files
> encrypted and stored entirely within your browser.

SDR (Secure Document Repository) は、Web Crypto API と IndexedDB
を利用した **完全ローカル動作の暗号化ドキュメント管理システム**です。

ファイルはブラウザ内で暗号化されて保存され、外部サーバーへ送信されることはありません。

## ✨ Features

### 🔐 Client-Side Encryption

-   AES-256-GCM による強力な暗号化
-   Web Crypto API を使用
-   ファイルごとに独立した暗号鍵を生成
-   復号はブラウザ内メモリ上のみで実施

### 🛡 Security First

-   マスターパスワード認証
-   PBKDF2（600,000 iterations）
-   HKDF による鍵派生
-   XSS対策済み
-   メモリゼロクリア処理
-   外部通信なし

### 📂 File Management

-   フォルダ階層管理
-   ドラッグ＆ドロップ対応
-   ファイル移動
-   名前変更
-   削除機能

### 👀 Preview Support

-   PDF
-   Image (PNG / JPG / GIF / WebP)
-   Text Files
-   Source Code Files

### 📦 Backup & Migration

-   SDR専用バックアップ形式
-   `.sdrpack` エクスポート
-   インポート機能
-   リポジトリ全体バックアップ
-   リストア機能

### 🎨 Modern UI

-   ダークモード
-   ライトモード
-   レスポンシブデザイン

## 🚀 Quick Start

``` bash
git clone https://github.com/yourname/SDR.git
```

ブラウザで `SDR.html` を開くだけで利用できます。

## 🔒 Security Model

  Component          Algorithm
  ------------------ --------------------------
  Master Key         PBKDF2-SHA256
  Key Derivation     HKDF
  File Encryption    AES-256-GCM
  Random Generator   crypto.getRandomValues()

## ⚠ Important Notes

-   IndexedDB に保存されます。
-   ブラウザデータ削除で保存データも消失します。
-   マスターパスワードを忘れると復号できません。

## 📄 License

MIT License
