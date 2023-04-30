<div align="center">
  <br />
    <p>
     <img src="https://github.com/191225/Unknown-Anti-Cheat/blob/alpha/pack_icon.png?raw=true" width="200" alt="Unknown Anti-Cheat Icon" /></a>
    </p>

**世界で最も高い検出力を誇るアンチチート**
# Unknown Anti-Cheat
Unknown Anti-CheatはScythe anti cheatをベースに開発しています。

<div align="left">
  
## セットアップ
アンチチートの設定はすべて `/scripts/data/config.js` で行うことができます。<br />
1. 設定から`Beta APIs`と`Education Edition`を有効にしてください。
2. アドオンをインポートせずにワールドを開いてください。（マルチプレイを無効にすることを推奨します）
> **Warning**: この手順を間違えるとワールド内すべてのNPCが削除されます。
3. すべてのNPCに`uac:bypassNPC`タグをつけてください。（`/tag @e[type=npc] add "uac:bypassNPC"`でタグをつけられます）
4. テレポートが行われるエリアの近くで`uac:bypass`タグがつくようにしてください。（`/tag @a[r=10] add "uac:bypass"`のような簡易的なものでも構いません）
5. アピールリンクを設定してください。
6. サーバー名を設定してください。
7. ルールを設定してください。
8. 権限レベルごとにパスワードを設定します。（推測できないパスワードにしてください）
9. コマンドを設定してください。
10. ホワイトリストを設定してください。（ゲーム内で有効にできます）
11. sanctuaryを設定してください。（デフォルトである設定をもとに設定してください）
12. 他のモジュールを設定してください。
13. アドオンをインポートしてください。（アンチチートはパックリストの最上位にある必要があります）
14. サーバーに入る前にデフォルトのゲームモードをアドベンチャーにするかGrief/Dを無効にしてください。（クリエイティブによるGrief/Gの検出対策）
15. `!op <password>`コマンドを使用して権限を取得してください。
16. `!ui`でuiを開き、`Server Options`の`Ban Modules`と`Whitelist`を設定してください。（オプション）
17. `!notify`でアンチチートの通知を有効にしてください。（オプション）
18. 保護されたサーバーで遊びましょう！

### 罰システム
これは`/scripts/data/config.js`の中で設定できます。<br />
> **punishment**<br />
> `mute` プレイヤーをミュートします。<br />
> `disconnect` プレイヤーをサーバーから切断します。<br />
> `kick` プレイヤーをサーバーから追放します。<br />
> `ban` プレイヤーをサーバーからBANします。<br /><br />
> **type**<br />
> `hacking` プレイヤーをハッキングしたとして処理します。（サーバーへの攻撃のときに使われます）<br />
> `cheating` プレイヤーをチート使用として処理します。（他プレイヤーとの不当な優位性があるときに使われます）<br />
> `silent` ログを出さずに処理します。<br /><br />
> **reason**<br />
> ここはカスタムです。<br /><br />
> **time**<br />
> `数字`+`d/h/m/s` 罰の時間を設定します。（`1m`, `10d`, `24h`）<br /><br />
> **heat**<br />
> `数字` Automatic Cheat Detectionのヒート（熱）を追加します。
  
## Unknown Anti-Cheatで検出されたハッキングのリスト
### BadEnchants
  > **A)** エンチャントレベルがバニラの上限を超えていないことをチェックします。<br />
  > **B)** エンチャントレベルがマイナスかチェックします。<br />
  > **C)** アイテムに適用できないエンチャントがあるかチェックします。<br />
  > **D)** アイテムにloreがあるかどうかをチェックします。<br />
  > **E)** マルチプロテクションアーマーであるかチェックします。<br />
  > **F)** 競合するエンチャントがあるかチェックします。

### BadPackets
  > **1)** プレイヤーの視点が無効かチェックします。<br />
  > **2)** メッセージの長さが無効かチェックします。<br />
  > **3)** 自身を殴っていないかチェックします。<br />
  > **4)** 現在選択されているスロットが無効かチェックします。<br />
  > **5)** 名前の長さが無効かチェックします。<br />

### CommandBlockExploit
  > **A)** インベントリから動物のバケツ・蜂の巣を削除します。<br />
  > **B)** 蜂の巣や蜂の巣箱を空気で置き換えます。<br />
  > **C)** コマンドブロックのマインカートがスポーンしたらkillします。<br />
  > **D)** 許可されていないNPCをkillします。<br />
  > **E)** コマンドブロックのマインカートのデスポーン時間をインスタント化します。<br />
  > **F)** 蜂の巣、蜂の巣箱、movingblockの設置を防止します。<br />
  > **G)** 追加のスポーンチェック。<br />
  > **H)** 追加のインベントリチェック。

### Crasher
  > **A)** 座標が無効かチェックします。<br />
  > **B)** データ値が無効の矢がドロップしたかチェックします。<br />
  > **C)** データ値が無効の矢を所持しているかチェックします。<br />
  > **D)** クラッシュする可能性のある看板が設置されたかチェックします。

### IllegalItems
  > **A)** プレイヤーのインベントリに不正アイテムがないかチェックチェックします。<br />
  > **B)** 不正なドロップアイテムを削除します。<br />
  > **C)** バニラのスタック上限を超えてるアイテムをチェックします。<br />
  > **D)** バニラでは取得できないアイテムをチェックします。<br />
  > **E)** 不正アイテムの設置をチェックします。<br />
  > **F)** アイテム名が上限を超えてるアイテムをチェックします。<br />
  > **G)** すでにアイテムの入ったチェストを設置したかチェックします。<br />
  > **H)** すでにアイテムの入ったトロッコやボートを設定したかチェックします。

### GIve
  > **A)** 不正な方法でアイテムを取得したかチェックします。（クラフトによる誤検出があります）

### Grief
  > **A)** インベントリにグリーフアイテムがあるかチェックします。<br />
  > **B)** グリーフアイテムを設置したかチェックします。<br />
  > **C)** TNT、エンドクリスタルがスポーンしたかチェックします。<br />
  > **D)** ゲームモードが不正かチェックします。

### Spam
  > **A)** 短時間に何回もメッセージを送信してるかチェックします。<br />
  > **B)** 重複したメッセージを何回も送信してるかチェックします。<br />
  > **C)** 長すぎるメッセージを送信しているかチェックします。<br />
  > **D)** 追加のスパムチェック。

### Spammer
  > **A)** 動きながらメッセージを送信してるかチェックします。<br />
  > **B)** 殴りながらメッセージを送信してるかチェックします。<br />
  > **C)** アイテムを使用しながらメッセージを送信してるかチェックします。<br />
  > **D)** チェストを開きながらメッセージを送信してるかチェックします。<br />
  > **E)** ジャンプしながらメッセージを送信してるかチェックします。

### MorePackets
  > **1)** 短時間に何度も検出しているかチェックします。<br />
  > **2)** 視点のスピードが速すぎるかチェックします。<br />
  > **3)** 短時間に複数のブロックを破壊してるかチェックします。<br />
  > **4)** horionのfree cameraをチェックします。<br />
  > **5)** ラグいアイテムを持っているかチェックします。<br />
  > **6)** 1tickに大量の矢を発射したかチェックします。<br />
  > **7)** Yの移動速度が一定かチェックします。

### NameSpoof
  > **A)** 名前の長さが不正かチェックします。<br />
  > **B)** ゲーマータグに使用できない文字が含まれてるかチェックします。<br />
  > **C)** 前回の参加時と名前が違うかチェックします。

### Nuker
  > **A)** 短時間に大量のブロックを破壊したかチェックします。

### AutoTool
  > **A)** ブロック破壊の始めと終わりのスロットが違うかチェックします。<br />
  > **B)** 追加のAutoToolチェック。<br />
  > **C)** ブロック破壊の始めにスロットを変えてるかチェックします。

### AirJump
  > **A)** ジャンプ中の動きが不正かチェックします。<br />
  > **B)** 追加のAirJumpチェック。
  > **C)** 追加のAirJumpチェック。

### AutoArmor
  > **A)** チェストを開きながらアーマーを装備しているかチェックします。<br />
  > **B)** 1tickに複数のアーマーを装備しているかチェックします。

### AutoClicker
  > **A)** エンティティへのクリックに対して1秒間のクリック数をチェックします。<br />
  > **B)** エンティティへのクリックに対してCPSの精度をチェックします。<br />
  > **C)** エンティティへのクリックに対して0.2秒間のクリック数をチェックします。<br />
  > **D)** エンティティへのクリックに対して追加の精度チェック。<br />
  > **E)** 1秒間のクリック数をチェックします。<br />
  > **F)** CPSの精度をチェックします。<br />
  > **G)** 0.2秒間のクリック数をチェックします。<br />
  > **H)** 追加の精度チェック。

### AutoShield
  > **A)** 移動中に盾を装備しているかチェックします。<br />
  > **B)** アイテムの使用中に盾を装備しているかチェックします。<br />
  > **C)** 殴ってるときに盾を装備しているかチェックします。

### AutoTotem
  > **A)** 移動中にトーテムを装備しているかチェックします。<br />
  > **B)** アイテムの使用中にトーテムを装備しているかチェックします。<br />
  > **C)** 殴ってるときにトーテムを装備しているかチェックします。

### Breaker
  > **A)** 視点先にないブロックを破壊しているかチェックします。

### ClickTP
  > **A)** スニークしたときに遠くへ移動したかチェックします。

### FastPlace
  > **A)** 短時間に大量のブロックを置いているかチェックします。<br />
  > **B)** 追加のFastPlaceチェック。

### FireInteract
  > **A)** 炎を破壊しているかチェックします。

### Fly
  > **A)** Flyのような動きをチェックします。<br />
  > **B)** 長時間空中にいるかチェックします。<br />
  > **C)** Y座標の振れ幅が大きいかチェックします。<br />
  > **D)** Y座標の移動スピードが不正かチェックします。<br />
  > **E)** Javaと同じ方法でFlyをチェックします。<br />
  > **F)** 水平移動よりもY移動が速いかチェックします。<br />
  > **G)** Y座標が一定の状態で水平移動しているかチェックします。<br />
  > **H)** 空中にいるのに移動速度が速いかチェックします。<br />
  > **I)** 空中にいる状態で落下していないかチェックします。

### InstantBreak
  > **A)** 一瞬でブロックを破壊しているかチェックします。

### JavaSneak
  > **A)** 1.5ブロックの隙間を通っているかチェックします。

### JetPack
  > **A)** JetPackのような動きをチェックします。

### Jesus
  > **A)** 水上での動きが不正かチェックします。<br />
  > **B)** 追加のJesusチェック。<br />
  > **C)** 水上に戻ろうとしているかチェックします。

### KillAura
  > **A)** アイテムを使用しながら殴っているかチェックします。<br />
  > **B)** 睡眠中に殴っているかチェックします。<br />
  > **C)** チェストを開きながら殴っているかチェックします。<br />
  > **D)** 1tickに複数のエンティティを殴っているかチェックします。<br />
  > **E)** 視点先にないエンティティを殴っているかチェックします。<br />
  > **F)** KillAuraに近い視点の動きをしているかチェックします。

### LiquidInteract
  > **A)** 液体を破壊しているかチェックします。

### NoSlow
  > **A)** アイテム使用中にスピードが落ちていないかチェックします。<br />
  > **B)** 追加のNoSlowチェック。<br />
  > **C)** 追加のNoSlowチェック。

### NoSwing
  > **A)** エンティティを攻撃したときに殴ったモーションがないかチェックします。<br />
  > **B)** ブロックを攻撃/破壊したときに殴ったモーションがないかチェックします。

### Phase
  > **A)** フルブロックの中にいるかチェックします。<br />
  > **B)** フルブロックを通過したか計算してチェックします。<br />
  > **C)** 追加のPhaseチェック。

### Reach
  > **A)** 遠くにいるエンティティを殴ったかチェックします。<br />
  > **B)** 遠くにあるブロックを破壊したかチェックします。<br />
  > **C)** ブロックを遠くに設置したかチェックします。

### Scaffold
  > **A)** 短時間に大量のブロックを設置しているかチェックします。<br />
  > **B)** 通常では設置できない位置にブロックを設置しているかチェックします。<br />
  > **C)** 斜めに移動しながらブロックを設置しているかチェックします。<br />
  > **D)** 他のことをしながらブロックを設置しているかチェックします。<br />
  > **E)** 設置したブロックと手に持ってるアイテムが異なるかチェックします。<br />
  > **F)** ブロックの設置中にスロットが変わってるかチェックします。

### Speed
  > **A)** 走った状態で移動スピードが不正かチェックします。<br />
  > **B)** 歩いた状態で移動スピードが不正かチェックします。<br />
  > **C)** スニーク状態で移動スピードが不正かチェックします。<br />
  > **D)** あらゆる状態で移動スピードが不正かチェックします。

### Sprint
  > **A)** 盲目が付いた状態で走っているかチェックします。<br />
  > **B)** アイテムを使用しながら走っているかチェックします。<br />
  > **C)** スニークしながら走っているかチェックします。<br />
  > **D)** 滑空中に走っているかチェックします。

### Step
  > **A)** ブロックの段差をジャンプせずに乗り上げているかチェックします。

### Teleport
  > **A)** 突然遠くに移動したかチェックします。

### NoFall
  > **A)** NoFallのような動きをチェックします。

### Xray
  > **A)** 周りに松明が無い状態で鉱石を破壊しているかチェックします。<br />
  > **B)** 短時間に大量の鉱石を破壊しているかチェックします。

## 他のモジュール

### ホワイトリスト
リストに追加されたプライヤー以外が入ると追放されます。<br />
これは`/scripts/data/config.js`で設定できます。

### グローバルBAN
既知のハッカーからサーバーを保護します。

### 追放投票
プライヤーを追放するのに投票します。<br />
アンチチートが反応しなかったり、管理者の対応が見込めない場合に使用されます。

### 自動チート検出
自動でチートを使用したユーザーを罰します。

### カラーチャットの無効化
セクションを使用したカラーチャットを無効化します。<br />
カラーチャットを使用したスパムを抑制します。<br />
これにより他のアドオンのカスタムコマンドに影響を出す可能性がありますが、メッセージの一番最初に`§r`が追加されただけです。

### 重複文字
メッセージ内の文字が重複してる場合、その文字を短くします。<br />
例: `wwwwwwwwwwwwwwwwwwwwww` => `www`

### ブロックロギング
プレイヤーの設置したブロックや破壊したブロックを記録します。<br />
`!inspect`で確認できます。<br />
設定ファイルで`type: 0`にした場合、永久保存になります。<br />
設定ファイルで`type: 1`にした場合、一時保存になります。（推奨）

### 大量検出
なんども検出するプレイヤーに警告します。<br />
この警告画面は非常に怖いものであり、無効にすることをおすすめします。

### リセットアイテムデータ
アイテムのデータをリセットします。

### ワールドボーダー
設定した範囲から出るとダメージを受けます。<br />
ボーダーからと遠ざかるにつれてダメージは大きくなります。

### AFK
AFKしているプレイヤーをサーバーから切断します。

### チャットフィルター
特定の語句が含まれている場合、メッセージの送信を取り消し、警告します。

### サンクチュアリ（保護エリア）
範囲内のエリアを保護します。<br />
この保護は非常に強力なものであり、チェストが開けなくなるなど、フルカスタマイズができます。