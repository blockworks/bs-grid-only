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

### よく使う色を変数として用意

```
$white:    #fff;
$gray-100: #e5e5e5;
$gray-200: #cccccc;
$gray-300: #b2b2b2;
$gray-400: #999999;
$gray-500: #808080;
$gray-600: #666666;
$gray-700: #4d4d4d;
$gray-800: #333333;
$gray-900: #1a1a1a;
$black:    #000;

//bs4準拠色
$blue:    #007bff;
$indigo:  #6610f2;
$purple:  #6f42c1;
$pink:    #e83e8c;
$red:     #dc3545;
$orange:  #fd7e14;
$yellow:  #ffc107;
$green:   #28a745;
$teal:    #20c997;
$cyan:    #17a2b8;
```

### widthとheightに33.33333%を追加

bs4では、幅や高さを調整するためのクラスが用意されていますが、そこに33.33333%を追加しました。

```
<div class="w-33"></div>
<div class="h-33"></div>
```

### margin、paddingのサイズを変更

bs4では、marginやpaddingのサイズを変更できるクラスが用意されていますが、それらの値を変更しました。

※その他margin全般（mx、my等）、padding 全般も全て用意されています。

|     | bs4標準 | bs4＋追加 |
|-----|---------|-----------|
| m-0 | 0       | 0         |
| m-1 | 0.25rem | 0.25rem   |
| m-2 | 0.5rem  | 0.5rem    |
| m-3 | 1rem    | 1rem      |
| m-4 | 1.5rem  | 1.5rem    |
| m-5 | 3rem    | 2rem      |
| m-6 | 無      | 2.5rem    |
| m-7 | 無      | 3rem      |


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

