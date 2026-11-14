# Bài tập Thiết kế Web

Thư mục này chính là gốc của trang GitHub Pages `<username>.github.io`. Mọi thứ bên trong được chép nguyên vào repo đó.

```
index.html                trang chủ, dẫn tới từng bài
images/
├── favicon.png           biểu tượng trên tab trình duyệt
└── ho-ca.jpg             ảnh bìa của bài Hồ cá trên trang chủ
HO_CA_VUI_NHON/           bài 6.1.1
├── images/
│   ├── diver1.png, diver2.png, diver3.png   thợ lặn (ảnh của sách)
│   ├── shark.png, turtle.png                cá mập, rùa (ảnh của sách)
│   ├── faintSchool.png, goldFishSchool.png  đàn cá (ảnh của sách)
│   ├── nen1.svg ... nen4.svg                4 cảnh nền tự vẽ
│   ├── rong1.svg, rong2.svg                 rong biển tự vẽ
│   └── favicon.png                          biểu tượng trên tab
├── audio/
│   └── bien-xanh.mp3                        nhạc nền tự soạn
├── ho_ca.html                               nội dung trang
└── mystyle.css                              định dạng và hiệu ứng chuyển động
```

## Bài 6.1.1: Hồ cá vui nhộn

- Ba thợ lặn lặn xuống rồi nổi lên. Mỗi người một tốc độ: 14, 18 và 22 giây một vòng.
- Cá mập bơi nhanh nhất (10 giây một vòng). Đàn cá vàng 16 giây, đàn cá xanh ở xa 30 giây, rùa chậm nhất 36 giây.
- Con nào chạm tường cũng quay đầu bơi lại (lật ảnh bằng `transform: scaleX(-1)`).
- Bong bóng chỉ đi lên, càng lên càng to rồi vỡ ở mặt nước. Rong biển đung đưa.
- Các nút ở góc trên bên phải màn hình:
  - **Đổi cảnh nền**: 4 cảnh thay phiên nhau (Biển xanh, Rạn san hô, Hoàng hôn, Biển đêm).
  - **Bật nhạc / Tắt nhạc**.
  - **Tạm dừng / Bơi tiếp**: dùng `animation-play-state`.
- Nút **← Trang chủ** ở góc trên bên trái để quay về `index.html`.

Trong `mystyle.css`, mỗi mốc % của `@keyframes` có ghi chú bên cạnh: giây thứ mấy và con vật bơi tới đâu. Ví dụ cá mập (10 giây một vòng):

| Mốc | Giây | Cá mập ở đâu |
|---|---|---|
| 0% | 0 | Sát tường trái, giữa hồ, mặt quay sang phải |
| 15% | 1,5 | Bơi được 25% quãng đường, ngoi lên |
| 30% | 3 | Bơi được 55% quãng đường, lặn xuống |
| 49.9% | 5 | Chạm tường phải |
| 50% | 5 | Quay đầu sang trái |
| 65% | 6,5 | Còn 70% quãng đường, ngoi lên cao |
| 80% | 8 | Còn 35% quãng đường, lặn xuống thấp |
| 100% | 10 | Về tới tường trái, vòng sau quay đầu lại |

## Thêm bài mới vào trang chủ

Trong `index.html`, chép khối `<li class="the">` của bài 6.1.1 rồi đổi đường dẫn, ảnh bìa, số bài, tên bài và mô tả.

## Nguồn tài nguyên

- Ảnh con vật: tài nguyên của sách, https://comp1802.github.io/ch06/aquarium.zip. Riêng `shark.png` đã được làm sạch viền trắng lởm chởm quanh thân (do ảnh gốc từng nằm trên nền trắng); hình cá mập giữ nguyên.
- Cảnh nền, rong biển, biểu tượng tab và nhạc nền "Biển xanh": tự làm riêng cho bài này, không lấy của ai nên không lo bản quyền.
