
# 設定 GOPATH

在使用任何第三方的套件, 都需要先設定 GOPATH

以 [goquery](https://github.com/PuerkitoBio/goquery) 這個第三方套件為例子

當沒有設定GOPATH就直接輸入

```
go get github.com/PuerkitoBio/goquery
```

會顯示

```
cannot download, $GOPATH not set. For more details see: go help gopath
```

表示要你下載前先設定好 GOPATH , 以下為設定步驟

```
mkdir goquery
export GOPATH=$HOME/goquery
```

這樣就設定好 goquery 的 GOPATH 了

然後切換到 goquery 目錄, 再抓下 goquery 就可以使用了

```
cd goquery
go get github.com/PuerkitoBio/goquery
```

=======================================================

GOPATH 就是要告訴編譯器在找套件的目錄的預設路徑

假設 GOPATH 有

```
user/aaa/
user/bbb/
```

當在 go 程式碼中 import "github.com/PuerkitoBio/goquery"

編譯器就會在 GOPATH 和你的 import 路徑串起來, 然後再這些路徑中

```
user/aaa/github.com/PuerkitoBio/goquery
user/bbb/github.com/PuerkitoBio/goquery
```

找你所要使用的套件