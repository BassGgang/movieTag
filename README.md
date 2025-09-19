# movieTag

University of Tokyo , TV program, Tag making application

## 概要

このアプリケーションは、講義動画をアップロードすると、AIが自動で文字起こしを行い、内容を要約して関連キーワードを10個生成します。

## 動作要件

*   Python 3.8以上
*   ffmpeg

## セットアップ

1.  **リポジトリをクローンします。**

    ```bash
    git clone https://github.com/your-username/movieTag.git
    cd movieTag
    ```

2.  **必要なライブラリをインストールします。**

    ```bash
    pip install -r requirements.txt
    ```

3.  **ffmpegを準備します。**

    *   [ffmpegの公式サイト](https://ffmpeg.org/download.html) から、お使いのOSに合ったffmpegをダウンロードしてください。
    *   ダウンロードした `ffmpeg.exe` と `ffprobe.exe` を、このリポジトリのルートディレクトリ（`app.py` と同じ場所）に配置してください。

## 設定

1.  **APIキーを設定します。**

    *   プロジェクトのルートディレクトリに `.env` という名前のファイルを作成します。
    *   `.env` ファイルに、以下のようにご自身のGemini APIキーを記述します。

    ```
    API_KEY="YOUR_GEMINI_API_KEY"
    ```

    ** `.env` ファイルは `.gitignore` に追加されているため、Gitリポジトリには含まれません。


## 実行方法

以下のコマンドを実行して、Streamlitアプリケーションを起動します。

```bash
streamlit run app.py
```

ブラウザで http://localhost:8501 が開かれ、アプリケーションにアクセスできます。
