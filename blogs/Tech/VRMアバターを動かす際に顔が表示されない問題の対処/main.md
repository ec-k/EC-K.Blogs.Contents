# VRM アバターを動かす際に顔が表示されない問題の対処

## 環境

Unity 2022.03f22

## 再現方法

アバターを `var bone = Animator.GetBoneTransform()`の bone に対する position, rotation への値の代入によって動かすこと

## 原因

アバターの Face などは動かないため，Bounds が置き去りになる．
アバターが大きく動くとき，それに追従したカメラが Face の Bounds を画角から外すことで描写されなくなる（Hair などについても同様）．

### 補足：Bounds とは

それがカメラ内にあるうちは，描画してくれるというもの

## 対処

- [ControlRig](https://vrm.dev/api/humanoid/Vrm10RuntimeControlRig/)で動かそう
  - 要検証．これでうまくいくかどうか分からん
- （それでだめなら，「Face も連動させよう」）

## References
