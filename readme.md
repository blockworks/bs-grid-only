# bootstrap4 Grid base template

bootstrap4（以下bs4）のgrid周りを抜き出し＋独自クラスを追加したファイル群です。

## ファイル概要

* style.scss　個別スタイルはこのファイルの「styles」以下に記述します
* _bootstrap-grid.scss　bs4のグリッドに関連したファイルです。bs4そのものです。
* _add-bs-custom.scss　bs4をベースに機能を追加したクラス群です。

## 独自機能

### メディアクエリをmixinにて追加可能

メディアクエリをmixinにて追加可能です。サイズは以下の通りです。

* xs 576px以下
* sm 768px以下（default）
* md 992px以下
* lg 1200px以下
* xl 1201px以上

```
@include mq(★){
  //add class
}
★にはxs、sm、md、lg、xlのいずれかを挿入
```

### widthとheightに33.33333%を追加

bs4では、幅や高さを調整するためのクラスが用意されていますが、33.33333%を追加しました。

```
<div class="w-33"></div>
<div class="h-33"></div>
```

## bs4 gridにはいろいろなクラスが用意されている

bs4のgridには「container、row、col、offset」などが有名ですが、実はいろいろなクラスが標準で用意されています。詳しくはソースを見ていただくといいですが、例えば、以下のようなものまで用意されています。クラス名でなんとなくイメージができると思います。

* .float-left
* .float-right
* .float-none
* .overflow-auto
* .overflow-hidden

* .d-none dはdisplay
* .d-inline
* .d-inline-block
* .d-block
* .d-table

* .position-static
* .position-relative
* .position-absolute
* .position-fixed

* .d-flex
* .d-inline-flex
* .flex-row
* .flex-column
* .flex-row-reverse
* .flex-column-reverse

* .justify-content-start
* .justify-content-end
* .justify-content-center
* .justify-content-between
* .justify-content-around

* .w-25、.w-33、.w-50、.w-75、.w-100、.w-auto
* .h-25、.h-33、.h-50、.h-75、.h-100、.h-auto

* .text-nowrap
* .text-wrap

* .font-weight-light   //300
* .font-weight-lighter   //lighter
* .font-weight-normal   //400
* .font-weight-bold   //700
* .font-weight-bolder   //bolder

* .rounded
* .rounded-sm
* .rounded-lg
* .rounded-circle
* .rounded-pill
* .rounded-0
* .rounded-top
* .rounded-right
* .rounded-bottom
* .rounded-left

