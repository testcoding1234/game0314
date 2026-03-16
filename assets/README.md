# ゲームアセット集 / Game Assets

ライセンス: **CC0 1.0 パブリックドメイン** — 登録不要・商用利用可・帰属表示不要

> These assets are original works dedicated to the public domain under CC0 1.0.
> Free for commercial use, no registration or attribution required.

---

## 📁 ディレクトリ構成 / Directory Structure

```
assets/
├── images/     SVG画像スプライト (64×64 viewBox)
├── sounds/     WAV効果音 (44100 Hz, 16-bit mono)
└── LICENSE     CC0ライセンス全文
```

---

## 🖼️ 画像一覧 / Image List

| ファイル | 内容 | 対象ゲーム |
|---|---|---|
| `hero.svg` | 魔法使い / Mage hero | 勇者の塔 |
| `enemy.svg` | スライム敵 / Slime enemy | 勇者の塔 |
| `boss.svg` | ドラゴンボス / Dragon boss | 勇者の塔 |
| `sword.svg` | 剣 / Sword weapon | 勇者の塔 |
| `shield.svg` | 盾 / Shield | 勇者の塔 |
| `tower.svg` | 城塔 / Castle tower | 勇者の塔 |
| `crown.svg` | 王冠（ボス印）/ Crown | 勇者の塔 |
| `potion.svg` | 回復ポーション / Potion | 勇者の塔 |
| `snowflake.svg` | 雪の結晶 / Snowflake | スノーサバイバル |
| `fire.svg` | 焚き火 / Campfire | スノーサバイバル |
| `axe.svg` | 斧（狩猟道具）/ Axe | スノーサバイバル |
| `tube.svg` | 試験管 / Test tube | カラーソート |
| `coin.svg` | 金貨 / Gold coin | 共通 |
| `heart.svg` | ハート（HP）/ Heart | 共通 |
| `star.svg` | 星 / Star | 共通 |
| `chest.svg` | 宝箱 / Treasure chest | 共通 |
| `explosion.svg` | 爆発エフェクト / Explosion | 共通 |

### 使い方 / Usage

```html
<img src="assets/images/hero.svg" width="64" height="64" alt="Hero">

<!-- CSSで背景として -->
<div style="background-image: url('assets/images/star.svg')"></div>
```

---

## 🔊 効果音一覧 / Sound Effect List

| ファイル | 内容 | 長さ | 用途 |
|---|---|---|---|
| `click.wav` | UIクリック音 / UI click | 0.06s | ボタン押下 |
| `hit.wav` | 攻撃ヒット音 / Attack hit | 0.18s | 戦闘ヒット |
| `coin.wav` | コイン取得音 / Coin pickup | 0.22s | アイテム取得 |
| `success.wav` | ステージクリア / Stage clear | 0.65s | 勝利・クリア |
| `gameover.wav` | ゲームオーバー / Game over | 0.75s | 失敗・終了 |
| `powerup.wav` | パワーアップ / Power up | 0.50s | レベルアップ |
| `whoosh.wav` | スイング音 / Whoosh/swing | 0.30s | 攻撃・移動 |

### 使い方 / Usage

```html
<!-- HTML Audio要素 -->
<audio id="sndClick" src="assets/sounds/click.wav" preload="auto"></audio>
<script>
  document.getElementById('sndClick').play();
</script>

<!-- Web Audio API -->
<script>
  const ctx = new AudioContext();
  const res = await fetch('assets/sounds/hit.wav');
  const buf = await res.arrayBuffer();
  const audioBuf = await ctx.decodeAudioData(buf);
  const source = ctx.createBufferSource();
  source.buffer = audioBuf;
  source.connect(ctx.destination);
  source.start();
</script>
```

---

## ライセンス詳細 / License Details

これらのアセットはすべて本プロジェクト用に新規制作したオリジナル作品です。
CC0 1.0 パブリックドメインとして公開しています。

- ✅ 商用利用可
- ✅ 改変・再配布可
- ✅ 帰属表示不要
- ✅ 登録不要

All assets are original works created for this project, released under CC0 1.0.
See `LICENSE` file for full license text.
