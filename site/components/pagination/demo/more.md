# 更多

- order: 1

更多分页。

---

````jsx
var Pagination = require('uxcore-pagination');

function onChange(page) {
  console.log(page);
}

ReactDOM.render(
  <Pagination onChange={onChange} total={500} />,
 document.getElementById('components-pagination-demo-more'));
````
