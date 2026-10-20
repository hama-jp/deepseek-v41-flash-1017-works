# DeepSeek V4.1 Flash 1017 — 3D制作の保存作品

DeepSeek V4.1 Flash 1017のEXL3 EAQ v1・2.9bpw版を、GB10搭載機2台とDeepSeek Harnessで動かした制作実験です。3作品のHTML、課題文、実行条件を共有します。

## 作品を開く

[ZIPをダウンロード](https://github.com/hama-jp/deepseek-v41-flash-1017-works/archive/refs/heads/main.zip)して展開し、`index.html`または`works/`内のHTMLをブラウザで開いてください。Three.jsを同梱した単一HTMLで、オフライン動作を確認しています。作品の再生にモデルの重みは必要ありません。

| 作品 | 保存ファイル | 状態 |
|---|---|---|
| ボクセル五重塔 | [voxel-pagoda.html](works/voxel-pagoda.html) | 塔・庭・昼夜表示。制御プロセス中断後、同じ締切内に再開 |
| 山間の鉄道模型 | [railway-original-2h.html](works/railway-original-2h.html) | 初回2時間の保存版。トンネルと車内視点などに未完成部分あり |
| 自由造形の五重塔 | [free-pagoda.html](works/free-pagoda.html) | Three.jsによる曲面の屋根・庭園・池 |

いずれも2時間枠で保存された作品で、期限までの最終完了応答はありません。鉄道と自由造形は2時間を連続実行しました。ボクセルの中断・再開は`conditions.json`に記録しています。後続の支援あり鉄道修正は、この3作品とは別です。

## 実行条件

- モデル：DeepSeek-V4.1-Flash-1017 / Mia AI Lab EXL3 EAQ v1 2.9bpw
- 実機：MSI EdgeXpert MS-C931とASUS GX10。各NVIDIA GB10、128GB統合メモリ
- 推論：TensorFold、2台に分割、並列要求1、DSpark有効
- ハーネス：DeepSeek Harness 0.2.1-rc.2
- 設定：context524288、max output262144、high、temperature1、top_p0.95、top_k20
- 各課題は空の独立した作業場所から開始。作品コードへの主担当の直接修正なし
- 残り90/60/30/15/5/2分を通知。通知の受領は応答中の処理により遅れることがあります

課題文は[prompts/](prompts/)、固定commit・重みrevision・作品SHA256・計測の定義は[conditions.json](conditions.json)、配布ファイルの検証用ハッシュは[SHA256SUMS](SHA256SUMS)にあります。同じ課題で同じ出力を保証するものではありません。

## 資料

- [指定レシピ：初回3作品で使った版](https://github.com/MiaAI-Lab/DeepSeek-v4.1-Flash-1017-2x-DGX-Sparks/tree/0e166b5f7dca029b5e98770a5c7a1c1c68531e65)
- [元モデル](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017)
- [使用した量子化版](https://huggingface.co/Mia-AiLab/DeepSeek-V4.1-Flash-1017-EXL3-EAQ-v1-2.9-bpw)

Three.jsのMITライセンスと帰属は[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)および[licenses/](licenses/)を参照してください。

This repository contains the three original saved HTML artifacts, prompts, pinned execution conditions and checksums. These are generated browser artworks, not model weights. The original railway artifact has known unfinished details; later assisted refinement is separate.
