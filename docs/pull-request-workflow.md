# Thực hành GitHub bằng một thay đổi có ích

Repo cá nhân này dùng để học branch, pull request và kiểm tra kết quả merge.
Không chứa mã nguồn Homeji hay thông tin đăng nhập.

## 1. Chọn một việc nhỏ

Ví dụ: bổ sung hướng dẫn cài đặt, sửa một đường dẫn hỏng hoặc thêm mẫu báo lỗi.
Viết kết quả mong muốn trước khi sửa. Một PR nên giải quyết một mục tiêu rõ ràng.

## 2. Tạo branch

```powershell
git clone https://github.com/thanhduykx/github-workflow-lab.git
cd github-workflow-lab
git switch main
git pull --ff-only
git switch -c docs/my-improvement
```

Nếu đã clone repo, bắt đầu từ bước chuyển về main. Dùng tên branch khác nếu tên đã tồn tại.

## 3. Sửa và kiểm tra

- Đọc lại toàn bộ nội dung thay đổi.
- Với tài liệu: kiểm tra lệnh, đường dẫn, bố cục và thông tin được khẳng định.
- Với mã nguồn: chạy kiểm tra phù hợp; ghi rõ phần chưa kiểm tra.
- Không commit token, mật khẩu, tệp .env hay dữ liệu riêng tư.

```powershell
git diff --check
git diff
git add docs/pull-request-workflow.md
git diff --cached
git commit -m "docs: clarify the pull request workflow"
git push -u origin docs/my-improvement
```

Thay đường dẫn trong lệnh git add bằng đúng tệp bạn đã sửa; tránh thêm tệp ngoài phạm vi.

## 4. Mở pull request

Chọn base main và branch vừa push. Mô tả vấn đề, kết quả thay đổi và bằng chứng kiểm tra.
Đọc tab Files changed. Với repo cộng tác hoặc sản phẩm đang chạy, tuân thủ quy tắc review và CI của repo.

## 5. Merge và xác minh

Chỉ merge khi thay đổi đã sẵn sàng. Sau đó xác nhận PR có trạng thái Merged và tệp xuất hiện trên main.
Tự merge tài liệu trong repo luyện tập có phạm vi ảnh hưởng nhỏ; dự án có người dùng cần quy trình kiểm tra tương ứng.

## 6. Ghi nhận thành tựu đúng với bằng chứng

GitHub Achievements do GitHub cấp, có thể cập nhật chậm và điều kiện có thể thay đổi.
Đã merge PR không đồng nghĩa đã được cấp huy hiệu: kiểm tra trực tiếp trên trang hồ sơ.

- Profile: https://github.com/thanhduykx?tab=achievements
- Tài liệu chính thức: https://docs.github.com/en/account-and-profile/reference/profile-reference#earning-achievements

Chỉ ghi đồng tác giả khi người đó thực sự đóng góp. Câu trả lời được chấp nhận và lượt star cần đến từ người dùng thật.
