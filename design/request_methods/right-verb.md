# Right Verb

---

在 HTTP 之中，共定義了一系列的請求方法，是以不同方式操作指定資源的動作，

而在 RESTful API 之中，需要使用這些動作，來表示如何對這些資源進行操作。

一般而言，對資源的操作行為大多是新增、查詢、修改、刪除這四種，

然而，這些定義於 HTTP 的動作，操作方式個個不同，

因此，在什麼情況下應該使用哪個動作將會是個重點，而這通常會由這些動作本身在 HTTP 中的定義來決定的。

各項動作與其在 HTTP 中的定義如下表所示：

| 動作類型 | 定義 |
| :--- | :--- |
| POST | 請求服務端接受傳送過去的請求內容，並以該請求內容為實體，新增新的子資源到 URI 所對應到的特定資源 |
| GET | 請求特定資源的表現形式 |
| PUT | 請求服務端接受傳送過去的請求內容，並以該請求內容為實體，請求將該實體存儲在客戶端請求的 URI 之下 |
| DELETE | 刪除特定資源 |

根據各項動作在 HTTP 中的定義，可以歸納幾個使用重點：

* GET 用於，僅用於查詢，而不該用於會引發其他效果的操作行為，像是修改或刪除之類的。

* DELETE 用於刪除特定資源，僅用於刪除。

* POST 用於新增資源，由客戶端。

* PUT：請求將封閉的實體存儲在提供的 URI 之下。
  由客戶端請求服務端接受傳送過去的請求內容，並以該請求內容為資源實體，要求服務端將該實體儲存在所請求的 URI 之下，
  換言之，如果所請求的 URI 對應的資源是存在著的，就用該實體替換掉原來對應到的資源，
  反之，如果所請求的 URI 對應的資源是不存在的，就用該實體作為新增的資源，讓 URI 對應到該資源。

