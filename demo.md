---
layout: page
title: Luận văn tốt nghiệp
subtitle: Phát hiện xe và phân đoạn đường trong ảnh sử dụng Deep Learning
---

### Trang web giúp người đọc có một cái nhìn chung về luận văn tốt nghiệp của nhóm


---
layout: post
title: Test markdown
subtitle: Each post also has a subtitle
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

Hình ảnh đầu vào cho mô hình

![Crepe](/img/um_000007.png)

Hình ảnh đầu ra tương ứng  

![Crepe](/img/um_000007_out.png)

{: .box-note}
**Note:** Hộp bao đóng được tô màu xanh dương quanh đối tượng được xác nhận, phía trên chữ vàng sẽ là tên đối tượng được đánh nhãn và độ chính xác của nó. Dòng chữ đỏ phía dưới sẽ là dự đoán khoảng cách của đối tượng này tới camera. Phần đường trên hình sẽ được phân đoạn và tô màu xanh lá cây (Hình ảnh được lấy trong bộ kiểm thử của tập dữ liệu KITTI).

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.
