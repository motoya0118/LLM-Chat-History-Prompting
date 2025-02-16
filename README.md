# LLM Chat History Prompting

## LLM の会話の仕組みを知りたい人へ 🤖✨

ChatGPT を使っていて、「なんで AI ってこんなに自然に会話できるんだろう？」と思ったことはありませんか？  
また、「ChatGPT だけじゃなく、OpenAI の API を使ったらもっと自由にカスタマイズできるの？」と気になったことは？  

このリポジトリでは、**生成 AI の会話が成立する仕組み** をシンプルに解説し、  
実際に OpenAI の API を使って **LLM を自由にカスタマイズする方法** を学べます！ 💡  

---

### 🎯 こんな人向け
- ChatGPT をなんとなく使ってるけど、どうして会話が成立してるのか気になる人  
- OpenAI の API を使うとどんなことができるのか試してみたい人  
- 生成 AI の仕組みを理解して、自分なりにカスタマイズしたい人  

---

### 📖 ここで学べること
- **生成 AI のチャットボットが会話を成立させる仕組み**
- **会話の流れを制御する "system プロンプト" の使い方**
- **発展編：LLM 同士を会話させてみる（AI バトル🔥）**

---

### 🚀 まずは試してみよう！
このリポジトリのコードを動かして、生成 AI の会話の裏側を覗いてみましょう！ 😆


## 環境セットアップ

このプロジェクトは `venv` を使用して仮想環境をセットアップします。

### 1. 仮想環境の作成
```sh
python -m venv venv-llm-chat
```

### 2. 仮想環境の有効化
**Windows:**
```sh
venv-llm-chat\Scripts\activate
```

**Mac/Linux:**
```sh
source venv-llm-chat/bin/activate
```

### 3. 依存関係のインストール
```sh
pip install -r requirements.txt
```

### 4. `.env` ファイルの作成
APIキーなどの環境変数を設定するために `.env` ファイルを作成します。

```sh
touch .env
```

ファイル内に以下のように記述してください。
```ini
OPENAI_API_KEY=your-api-key-here
```

### 5. Jupyter Lab のセットアップと起動
Jupyter Lab を仮想環境で利用するには、以下の手順を実行してください。

1. 仮想環境を Jupyter のカーネルとして登録
```sh
python -m ipykernel install --user --name=venv-llm-chat --display-name "Python (venv-llm-chat)"
```

2. Jupyter Lab の起動
```sh
jupyter lab
```

3. Jupyter Lab 内でカーネルを選択
   - Jupyter Lab の右上の「Kernel」 → 「Change Kernel」から `Python (venv-llm-chat)` を選択

### 6. 環境の無効化 (終了時)
```sh
deactivate
```

## 使用ライブラリ
- `openai` (LLM APIの利用)
- `gradio` (インターフェース構築)
- `python-dotenv` (`.env` ファイルの管理)
- `jupyterlab` (ノートブック環境)
- `ipykernel` (仮想環境を Jupyter で使用するため)
