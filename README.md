# task-management-portfolio
# **README**  

---

# **📌 Googleスプレッドシート連携タスク管理ツール**  

## **📝 概要**  
Python を学習したアウトプットの一環として、**Googleスプレッドシートと連携できるタスク管理ツール** を開発しました。
プログラミング初学者のため、全て1人で完了というわけではなく書籍、ネットの知識を調べつつ、そしてエラーコードのレビュー、修正はAIも利用しつつ作成したものとなります。

コマンドでタスクを管理でき、**タスクの追加・一覧表示・完了・削除** などの機能を備えています。  
また、Googleスプレッドシートにタスクを保存し、複数デバイスからデータを管理することが可能です。  

---

## **🎯 このプロジェクトを作った理由**  
✅ **Python 学習のアウトプットとして実践的なアプリを作りたかった**  
✅ **Googleスプレッドシートを使って、タスク管理を簡単にできるようにしたかった**  
✅ **API を活用して、外部サービスと連携するスキルを身につけたかった**  

---

## **⚙️ 機能**
| 番号 | 機能 | 説明 |
|------|------|------|
| **1** | **タスクを追加** | タスク名・説明・期限・優先度を指定して追加 |
| **2** | **タスク一覧を表示** | ローカル・スプレッドシートのタスクを表示 |
| **3** | **タスクを完了** | 任意のタスクを完了し、削除するか選択可能 |
| **4** | **Googleスプレッドシートに保存** | ローカルタスクをスプレッドシートに同期（重複なし） |
| **5** | **終了** | タスク名・説明・期限・優先度を指定して追加 |

---

## **🛠 使用技術**
- **言語**: Python  
- **外部ライブラリ**:  
  - `gspread`（Google Sheets API 連携）  
  - `oauth2client`（Google API 認証）  
- **データストレージ**: Google スプレッドシート  
- **実行環境**: Google Colab  

---

## **🚀 環境構築 & 使い方**
### **1️⃣ 必要なもの**
- Google アカウント
- Google スプレッドシート（任意の名前で作成）
- Google Cloud Platform (GCP) の API 設定
- Python 実行環境（Google Colab）

### **2️⃣ Google Cloud Platform (GCP) 設定**
1. [Google Cloud Console](https://console.cloud.google.com/) にアクセスし、新しいプロジェクトを作成  
2. **Google Sheets API** と **Google Drive API** を有効化  
3. **サービスアカウントを作成**し、JSON 形式の認証キーをダウンロード  
4. **Google Drive に `credentials.json` をアップロード**  

#### **スプレッドシートの共有設定**
- **方法①**: 「リンクを知っている全員」に **編集者権限** を付与  
- **方法②**: `credentials.json` 内の `client_email` の値をコピーし、**サービスアカウントを編集者として追加**  

### **3️⃣ 必要なライブラリのインストール**
```bash
pip install gspread oauth2client
```

### **4️⃣ Google Drive をマウント（Google Colab 使用時）**
```python
from google.colab import drive
drive.mount('/content/drive')
```

### **5️⃣ 該当箇所を変更しスクリプトを実行**
**#Googleスプレッドシート認証**
```
credentials_path = "/content/drive/MyDrive/credentials.json"  # 必要に応じて修正
spreadsheet = gc.open("タスク管理ツール")  # 任意のスプレッドシート名に変更
```
🔗 **GitHub リポジトリ:** [https://github.com/MaiHirahara/task-management-portfolio](https://github.com/MaiHirahara/task-management-portfolio)  

---
