# 任意の言語の実行環境での文字エンコーディング指定方法まとめ

## シェル

参考: [シェルの文字コード設定 CapmNetwork](http://capm-network.com/?tag=%E3%82%B7%E3%82%A7%E3%83%AB%E3%81%AE%E6%96%87%E5%AD%97%E3%82%B3%E3%83%BC%E3%83%89%E8%A8%AD%E5%AE%9A)

### bash

export で指定する

```bash
export LANG=ja_JP.eucJP
```

### csh

setenv で指定する

```csh
setenv LANG ja_JP.SJIS
```

## HTML

参考: [HTML で文字エンコーディングを指定する](https://www.w3.org/International/questions/qa-html-encoding-declarations.ja)

meta タグの charset 属性で指定する。

```html
<meta charset="utf-8" />
```

## PHP

参考: [PHP: mb_internal_encoding - Manual](https://www.php.net/manual/ja/function.mb-internal-encoding.php)

mb_internal_encoding で指定する

```php
<?php
/* 内部文字エンコーディングをUTF-8に設定 */
mb_internal_encoding("UTF-8");

/* 現在の内部文字エンコーディングを表示 */
echo mb_internal_encoding();
?>
```
