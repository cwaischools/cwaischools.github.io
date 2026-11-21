# Banner ảnh khóa học

Thả file ảnh banner vào thư mục này, rồi khai báo trong `src/components/HeroBanner.tsx`
(mảng `BANNERS`), theo thứ tự muốn hiển thị:

```ts
export const BANNERS: Banner[] = [
  { src: '/banners/banner-khai-giang.jpg',
    alt: { vi: 'Mô tả ảnh', ja: '画像の説明', en: 'What the image shows' } },
  { src: '/banners/banner-uu-dai.jpg',
    alt: { vi: '…', ja: '…', en: '…' } },
];
```

Yêu cầu file:
- Kích thước khuyến nghị **1256 × 1432** (khung hero ở 1440px) hoặc lớn hơn, cùng tỉ lệ.
  Ảnh nhỏ hơn sẽ bị phóng to và checker báo `photo-upscale`.
- Định dạng `.jpg` hoặc `.webp`, dưới ~400 KB mỗi file.
- `alt` phải tả **nội dung ảnh**, không phải thông điệp marketing — đây là text màn hình đọc.

Khi có từ 2 banner trở lên, slider tự chạy 5 giây một ảnh, kèm nút tạm dừng và chấm chuyển.
Với 1 banner thì hiển thị tĩnh, không có điều khiển.
