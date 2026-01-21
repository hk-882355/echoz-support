# ECHOZ - スクリーンショット撮影ガイド

## 必要なサイズ

### 必須（最低1セット）
| デバイス | 解像度 | 対象機種 |
|---------|--------|---------|
| 6.7インチ | 1290 x 2796 px | iPhone 15 Pro Max, 16 Pro Max |
| 6.5インチ | 1284 x 2778 px | iPhone 14 Plus, 15 Plus |

### 推奨（古いデバイス対応）
| デバイス | 解像度 | 対象機種 |
|---------|--------|---------|
| 5.5インチ | 1242 x 2208 px | iPhone 8 Plus |

---

## 撮影する画面（6枚推奨）

### スクリーンショット 1: スプラッシュ / ヒーロー
**画面**: スプラッシュスクリーン or ホーム画面
**キャッチコピー**:
- 日本語: `今の気持ちを、そっと共鳴させる。`
- English: `Share your moment.`

### スクリーンショット 2: 投稿ウィンドウ
**画面**: 投稿画面（気分選択中）
**キャッチコピー**:
- 日本語: `その瞬間の感情を、言葉に。`
- English: `Capture how you feel.`

### スクリーンショット 3: タイムライン
**画面**: ホーム画面のタイムライン（複数投稿表示）
**キャッチコピー**:
- 日本語: `縦書きで、美しく。`
- English: `Beautiful vertical posts.`

### スクリーンショット 4: Echo Chain
**画面**: Echo Chainモーダル
**キャッチコピー**:
- 日本語: `同じ気持ちが、静かに繋がる。`
- English: `Connect through feelings.`

### スクリーンショット 5: プロフィール
**画面**: マイプロフィール画面
**キャッチコピー**:
- 日本語: `あなたの感情の記録。`
- English: `Your emotional journey.`

### スクリーンショット 6: 通知
**画面**: 投稿ウィンドウ通知ポップアップ
**キャッチコピー**:
- 日本語: `ランダムに届く、投稿のきっかけ。`
- English: `Random moments to share.`

---

## 撮影手順

### 1. シミュレーターで撮影
```bash
# Xcode Simulatorを起動
xcrun simctl list devices

# 6.7インチ用 (iPhone 15 Pro Max)
xcrun simctl boot "iPhone 15 Pro Max"

# スクリーンショット撮影
xcrun simctl io booted screenshot ~/Desktop/screenshot1.png
```

### 2. 実機で撮影
1. iPhone 15 Pro Max または iPhone 14 Plus を使用
2. 電源 + 音量上ボタン同時押し
3. 写真アプリから AirDrop でMacへ転送

### 3. デバイスフレーム追加（任意）
- **Rotato**: https://rotato.app
- **Mockup Generator**: https://mockuuups.studio
- **Screenshots Pro**: App Store

---

## テキストオーバーレイ作成

### Figma / Canva 推奨設定

**キャンバスサイズ**: 1290 x 2796 px

**フォント設定**:
- 日本語: Hiragino Sans W6 または SF Pro Display
- English: SF Pro Display Semibold
- サイズ: 72-96px
- 色: 白（#FFFFFF）+ シャドウ

**背景グラデーション案**:
```
案1（シアン系）: #0A1628 → #1E3A5F
案2（ダーク）: #000000 → #1A1A2E
案3（パープル）: #1A0033 → #330066
```

**レイアウト**:
```
┌─────────────────────┐
│                     │
│   キャッチコピー     │  ← 上部 20%
│                     │
│  ┌───────────────┐  │
│  │               │  │
│  │  スクリーン    │  │  ← 中央 70%
│  │  ショット     │  │
│  │               │  │
│  └───────────────┘  │
│                     │
│      ECHOZ         │  ← 下部 10%
│                     │
└─────────────────────┘
```

---

## ダミーデータ設定

### 投稿サンプル
```
今日は空が綺麗だった
```

```
コーヒーが美味しい朝
```

```
なんだか落ち着かない
```

```
嬉しいことがあった！
```

### 気分選択
- スクショ用おすすめ: 😊 Happy, 😌 Calm, 💭 Thinking

---

## チェックリスト

- [ ] ステータスバー: 時刻を 9:41 に設定（Apple公式）
- [ ] バッテリー: 100% 表示
- [ ] Wi-Fi/電波: フル表示
- [ ] ダークモード: ON（推奨）
- [ ] 通知バッジ: 非表示
- [ ] 個人情報: ダミーデータ使用

---

## 出力ファイル命名規則

```
ECHOZ_[言語]_[サイズ]_[番号]_[画面名].png

例:
ECHOZ_ja_6.7inch_01_splash.png
ECHOZ_ja_6.7inch_02_posting.png
ECHOZ_en_6.7inch_01_splash.png
```
