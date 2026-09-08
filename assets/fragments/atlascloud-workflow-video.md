# Atlas Cloud Workflow：動画生成の参考メモ

Atlas CloudのWorkflow機能をアンロックしてみたところ、動画生成用のAPIも用意されていた。動画生成の選択肢を探す際の参考として、確認した内容を残しておく。

## APIから取得できるもの

Workflow StudioにはAPIの案内があり、Workflowの一覧と、それぞれの入力項目・設定条件を示すスキーマを取得できる。

接続先は `https://api.atlascloud.ai`。手元のAPIキーを使ったBearer認証で、次の取得を確認した。

| 内容 | API | 確認結果 |
|---|---|---|
| Workflowの一覧 | `GET /api/v1/workflows` | 58件を取得 |
| 個別Workflowのスキーマ | `GET /api/v1/workflows/{workflow_name}` | Seedance 2.0のReference to Videoで取得成功 |

個別スキーマの取得に使ったWorkflow名は `seedance-2.0-reference-to-video-workflow`。どちらもHTTP 200で応答した。

## スキーマの内容

個別Workflowの応答には、`input_schema`（入力仕様）、`output_schema`（出力仕様）、`models`、`example`、`examples`、`nodes`、`edges`などが含まれていた。

Seedance 2.0のReference to Videoでは、次のような入力項目と条件を確認できた。

| 入力項目 | 内容・設定例 |
|---|---|
| `prompt` | 動画の指示文 |
| `reference_images` | 参照画像。最大9枚 |
| `reference_videos` | 参照動画。最大3本、合計15秒以下 |
| `reference_audio` | 参照音声 |
| `duration` | 動画の長さ。4〜15秒の指定など |
| `ratio` | `16:9`、`9:16`、`1:1`などの比率 |
| `resolution` | `480p`、`720p`、`1080p` |
| `generate_audio` | 音声生成の有無 |

このほか、透かしや最終フレームの返却に関する項目もあった。表は取得時のスキーマの抜粋で、すべての条件を載せたものではない。参照動画の上限は画面表示とスキーマに違いがあったため、ここではスキーマ側の値を記している。

## 動画生成の呼び出し

APIの案内では、生成の送信先は `POST /api/v1/model/generateVideo`、結果の照会先は `GET /api/v1/model/prediction/{id}` となっていた。

Reference to Videoの場合、生成時に指定するモデルIDは `atlascloud/workflow/seedance-2.0/reference-to-video`。スキーマ取得に使うWorkflow名とは別になっている。

生成リクエストの送り方まで用意されているが、今回確認したのは案内の内容と一覧・スキーマの取得までで、API経由のWorkflow動画生成はまだ試していない。

---

確認日：2026年9月1日

参照先：[Atlas Cloud Workflow Studio](https://www.atlascloud.ai/ja/console/workflow/studio)

アンロック済みアカウントで確認した個人のメモです。アンロック条件や他のアカウントでの利用可否は調べていません。仕様は確認当時のもので、利用時には最新の案内・スキーマを確認してください。
