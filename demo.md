---
layout: page
title: Luận văn tốt nghiệp
subtitle: Phát hiện xe và phân đoạn đường trong ảnh sử dụng Deep Learning
---

### Trang web giúp người đọc có một cái nhìn chung về luận văn tốt nghiệp của nhóm

Hình ảnh đầu vào cho mô hình

![Crepe](/img/um_000007.png)

Hình ảnh đầu ra tương ứng  

![Crepe](/img/um_000007_out.png)

{: .box-note}
**Chú ý:** Hộp bao đóng được tô màu xanh dương quanh đối tượng được xác nhận, phía trên chữ vàng sẽ là tên đối tượng được đánh nhãn và độ chính xác của nó. Dòng chữ đỏ phía dưới sẽ là dự đoán khoảng cách của đối tượng này tới camera. Phần đường trên hình sẽ được phân đoạn và tô màu xanh lá cây (Hình ảnh được lấy trong bộ kiểm thử của tập dữ liệu KITTI).


Đồng thời, một file json sẽ lưu đầy đủ các thông tin phát hiện được này để có thể đem đi sử dụng ở các ứng dụng khác, đây là ví dụ các thông tin cho hình ở trên:
{% highlight javascript linenos %}
2019-01-01 09:09:40,109 INFO 2 Cars detected
2019-01-01 09:09:40,286 INFO 
2019-01-01 09:09:40,286 INFO Coordinates of Box 0
2019-01-01 09:09:40,286 INFO     x1: 499.0
2019-01-01 09:09:40,286 INFO     x2: 553.0
2019-01-01 09:09:40,286 INFO     y1: 188.0
2019-01-01 09:09:40,287 INFO     y2: 224.0
2019-01-01 09:09:40,287 INFO     Confidence: 0.977694034576
2019-01-01 09:09:40,291 INFO     depth: 27.1126384735
2019-01-01 09:09:40,292 INFO 
2019-01-01 09:09:40,292 INFO Coordinates of Box 1
2019-01-01 09:09:40,292 INFO     x1: 606.0
2019-01-01 09:09:40,292 INFO     x2: 652.0
2019-01-01 09:09:40,292 INFO     y1: 180.0
2019-01-01 09:09:40,292 INFO     y2: 226.0
2019-01-01 09:09:40,292 INFO     Confidence: 0.977711379528
2019-01-01 09:09:40,296 INFO     depth: 24.5325317383
2019-01-01 09:09:40,515 INFO 
2019-01-01 09:09:40,515 INFO Output image has been saved to:
/home/g1413355/thesis/Semantic-Segmentation/TaiMultiNet/MultiNet/result/um_000007_out.png
{% endhighlight %}

Lệnh để thực hiện train model với các thông số như weights, hàm loss, batch_size, max_steps, ...:
```
python train.py --hypes hypes/multinet.json
```

Script sử dụng để kiểm thử trên tập dữ liệu KITTI:
```
./run_demo.sh `path_to_input` `path_to_output`
```

<details>
<summary>How do I dropdown?</summary>
<br>
This is how you dropdown.
<br><br>
<pre>
&lt;details&gt;
&lt;summary&gt;How do I dropdown?&lt;/summary&gt;
&lt;br&gt;
This is how you dropdown.
&lt;details&gt;
</pre>
</details>

{: .box-note}
**Chú ý:** Mô hình được train và các trọng số được lưu lại trên server được thuê từ google cloud nên chỉ demo được khi nhóm start server này. Vì vậy, việc muốn thực hiện được demo phải liên hệ với nhóm.

