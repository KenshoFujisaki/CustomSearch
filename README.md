CustomSearch
============

####これはなに？
独自の検索を手軽に行うためのvimperator向けコードです。
![Alt text](http://i.gyazo.com/8431f5201bf71c64304c983eae6b140e.png)

####使い方
_vimperatorrcファイルの内容を、ご自身の_vimperatorrcファイルにコピペすることで使えます．

####カスタマイズ
下にならって、_vimperatorrcにおける変数subcommandsのハッシュ配列に  
検索対象の検索エンジンを追加することで、簡単に拡張できます。
```javascript
/**
 * subcommandsにサブコマンド名(subcommand)、説明(description)、検索対象のURL(target_uri)を設定ください。
 * ただし、検索対象のURLについては、URLの最後に検索パラメータ（&q=や&s=）が来るようにしてください。
 * また、command.addUserCommandの中身については編集する必要はありません。
 */
let subcommands = [
  {
    subcommand: "github",
    description: "GitHub @ github.com",
    target_uri: "https://github.com/search?utf8=%E2%9C%93&q="
  }, {
    subcommand: "openhub",
    description: "open source code search @ code.openhub.net",
    target_uri: "http://code.openhub.net/search?s="
  }, {
    subcommand: "scholar",
    description: "google scholar search @ scholar.google.co.jp",
    target_uri: "http://scholar.google.co.jp/scholar?q="
  }
];
```
