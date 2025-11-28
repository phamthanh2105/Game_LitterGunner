# 🔫 Little Gunner

Game bắn súng góc nhìn từ trên xuống (top-down shooter) được xây dựng bằng Unity 2022.3 LTS.

## 🎮 Tính năng chính

### 🕹️ Hệ thống điều khiển
- **🚶‍♂️ Di chuyển linh hoạt**: Điều khiển nhân vật bằng `WASD`, ngắm bắn theo chuột với góc quay tự động
- **⚡ Dash chiến thuật**: Nhấn `Space` để lướt nhanh, tiêu hao 20 stamina, tạo hiệu ứng bóng mờ liên tục và bất tử trong thời gian dash (0.25 giây)
- **🔋 Quản lý thể lực**: Thanh stamina hiển thị trực quan, cần cân nhắc khi sử dụng dash để né đòn

### 🔫 Hệ thống vũ khí
- **🔫 Súng chính**: Bắn liên tục bằng chuột trái, sử dụng object pooling để tối ưu hiệu năng, hiệu ứng muzzle flash khi bắn
- **🚀 Rocket phụ**: Phóng rocket mạnh bằng chuột phải, số lượng giới hạn (mặc định 2), có thể nhặt thêm qua vật phẩm `ItemRocket`
- **🎁 Vật phẩm**: Hệ thống pickup item để bổ sung rocket trong trận đấu

### 👾 Hệ thống kẻ địch
- **♻️ Spawn động**: Kẻ địch xuất hiện ngẫu nhiên trong vùng spawn, tốc độ spawn tăng dần theo thời gian để tạo độ khó tăng tiến
- **🤖 AI đơn giản**: Kẻ địch di chuyển và tấn công người chơi, gây sát thương khi tiếp xúc
- **💢 Hiển thị sát thương**: Text nổi hiển thị damage khi bắn trúng, màu đỏ cho damage cao (>10)
- **💥 Hiệu ứng tử vong**: Particle effect khi kẻ địch bị tiêu diệt

### 🏆 Hệ thống điểm số & Thành tích
- **🎯 Điểm số real-time**: Cập nhật điểm ngay khi tiêu diệt kẻ địch
- **🥇 High Score**: Tự động lưu và so sánh điểm cao, hiển thị nhãn "High Score" khi đạt kỷ lục mới
- **📊 Leaderboard trực tuyến**: Tích hợp LeaderboardCreator để xem và cập nhật bảng xếp hạng online
- **📈 Thống kê trận đấu**: Hiển thị thời gian chơi, tổng điểm, số kẻ địch tiêu diệt khi game over
- **⭐ Hệ thống đánh giá**: Hiển thị mark/rating dựa trên điểm số đạt được

### 🖥️ Hệ thống UI/UX
- **❤️ Health Bar**: Thanh máu hiển thị trực quan, cập nhật real-time
- **🔋 Stamina Bar**: Theo dõi thể lực để sử dụng dash hiệu quả
- **🎯 Score Display**: Hiển thị điểm hiện tại và điểm cao nhất
- **☠️ Game Over Screen**: Màn hình kết thúc với animation, thống kê chi tiết và các nút chơi lại/thoát
- **📋 Menu chính**: Màn hình bắt đầu với các tùy chọn chọn map, xem hướng dẫn, xem leaderboard
- **🗺️ Chọn map**: Hệ thống chọn nhiều bản đồ khác nhau để chơi

### 🔊 Hệ thống âm thanh
- **🎵 Nhạc nền động**: Nhạc nền thay đổi khi trận đấu bước vào giai đoạn nguy hiểm (sau 100 giây)
- **🔊 Hiệu ứng âm thanh**: Âm thanh riêng cho bắn súng, phóng rocket, dash, va chạm, UI popup, v.v.
- **🎚️ Audio Manager**: Quản lý tập trung tất cả âm thanh trong game, tự động phát theo ngữ cảnh

## 🛠️ Yêu cầu
- Unity 2022.3.46f1 (LTS)

## ▶️ Cách chạy
1. Mở Unity Hub → Add project → chọn thư mục `LittleGunner`
2. Mở scene `Assets/Scenes/StartScene.unity`
3. Nhấn Play

## ⌨️ Điều khiển

| 🕹️ Hành động | 🖱️ Phím/Chuột |
|--------------|----------------|
| 🚶‍♂️ Di chuyển | `W` `A` `S` `D` |
| 🔫 Bắn súng | Giữ chuột trái |
| 🚀 Phóng rocket | Giữ chuột phải |
| ⚡ Dash | `Space` (tiêu 20 stamina) |

## 📁 Cấu trúc thư mục
- `Assets/Scripts/Player/` 🧍‍♂️ Điều khiển nhân vật, thể lực  
- `Assets/Scripts/Weapon/` 🔫 Súng, rocket, đạn  
- `Assets/Scripts/Enemy/` 👾 AI kẻ địch  
- `Assets/Scripts/ResScript/` ⚙️ Game manager, spawn, pooling, leaderboard  
- `Assets/Scripts/UI/` 🖥️ Thanh máu, stamina, điểm số  

## 🏗️ Build
1. `File → Build Settings`
2. Thêm các scene cần thiết
3. Chọn nền tảng và Build
