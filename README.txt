AhaFood.AI — WebAR (MindAR + PNG Robot)
=======================================

Files:
- index.html      → Trang WebAR (image tracking) dùng MindAR + A‑Frame
- robot.png       → Robot PNG (đã chuyển từ all-category.webp)
- targets.mind    → (Bạn cần tự tạo bằng MindAR Studio từ ảnh card/logo) – đặt cùng thư mục với index.html

Cách triển khai:
1) Vào MindAR Studio: https://hiukim.github.io/mind-ar-js-doc/tools/compile/
   - Chọn ảnh mục tiêu (trên card) → Compile → tải về targets.mind
   - Đổi tên đúng "targets.mind" và đặt cạnh index.html
2) Host thư mục này lên HTTPS (Netlify/Vercel/GitHub Pages)
3) Tạo mã QR trỏ tới URL của index.html
4) In QR lên card cùng với chính ảnh mục tiêu (đã dùng compile)
5) Khách quét QR → cấp quyền camera → đưa card vào khung → robot xuất hiện → bấm 📸 để chụp → 🛒 để đặt món

Ghi chú:
- Nên in ảnh mục tiêu kích thước >= 6–8 cm, bề mặt không bóng, nhiều chi tiết/hoa văn để tracking tốt.
- Nếu cần đổi kích thước/độ cao robot: sửa thuộc tính width/height/position của #robot trong index.html
- Nếu robot bị dính nền: dùng PNG nền trong suốt, và giữ "transparent: true; alphaTest: 0.05"
