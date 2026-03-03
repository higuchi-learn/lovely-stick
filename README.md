# ステキなステッキ 🪄

対戦型の組み込みゲームです。杖型コントローラーを振ってバトルします。

**技育CAMP ハッカソン vol.19 優秀賞（2位）／ 技育博2024 vol.6 株式会社ゆめみ企業賞**
<img width="1108" height="620" alt="image" src="https://github.com/user-attachments/assets/328c6f28-cc6a-489e-abb4-9fd2ea641dde" />

![alt text](image-3.png)
<img width="1084" height="568" alt="SnapCrab_No-0106" src="https://github.com/user-attachments/assets/a09384c2-9828-4d07-ab33-7206d0b33fa4" />

## 概要

Raspberry Pi Pico W を搭載した杖型コントローラーを使って、2人のプレイヤーが動きで対戦するゲームです。コントローラーのセンサー値をサーバーへ送信し、Webアプリ側でゲームの判定を行います。

## 背景

ハッカソンで「見ている人が楽しめるもの」を作ろうという方針から着想。ハードウェアとWebアプリを組み合わせることで、デモとして映えるプロダクトを目指しました。

## 技術スタック

| 領域 | 技術 |
|------|------|
| 組み込み | MicroPython / Raspberry Pi Pico W |
| 通信 | HTTP（擬似リアルタイム） |
| 電子回路 | センサー回路設計・実装 |

## 私の担当

- Raspberry Pi Pico W を用いたコントローラーの電子回路設計・実装
- センサー値をJSON形式でサーバーへ送信する通信処理の設計・実装

## 技術的な工夫

当初 WebSocket を使用する予定でしたが、MicroPython 環境では利用可能なWebSocketライブラリが存在しないことが判明しました。そこで **毎秒HTTP通信＋レスポンスの条件分岐** によって擬似リアルタイム通信を実装しました。ベストプラクティスでなくとも、制約の中で目的を達成する最適解を考える経験になりました。

## リンク

- 発表スライド: https://www.canva.com/design/DAGeeEF3T2U/qEBiPbFmTjxi5IjgVbHxjg/view
