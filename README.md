# Blogger Affiliate List

このリポジトリは、Bloggerテーマで使用するアフィリエイト商品リストを外部JSONファイルとして管理するためのものです。

## ファイル構成

- `affList.json` - 商品リスト（メインファイル）

## GitHub Pages設定

1. このリポジトリの Settings → Pages に移動
2. Source を `main` ブランチに設定
3. 公開URLは `https://YOUR_USERNAME.github.io/blogger-afflist/affList.json` になります

## 商品の追加方法

`affList.json` を編集して、以下の形式で商品を追加：

```json
{
  "product-id": {
    "name": "商品名",
    "image": "商品画像URL（オプション）",
    "rakuten": "楽天アフィリエイトURL",
    "amazon": "AmazonアフィリエイトURL"
  }
}
```

## ツールとの連携

`rakuten_amazon_finder.py` で商品を検索し、出力されたコードをこのJSONファイルに追加できます：

```bash
python autoblog/tools/rakuten_amazon_finder.py "商品名" --category book --output afflist
```

## 更新の反映

JSONファイルを更新してGitHubにpushすると、数分以内にBloggerサイトに反映されます。
