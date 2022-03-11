## Welcome to thuduyen07 GitHub Pages

You can also check out my social medias: 
- [thuduyen07-Github](https://github.com/thuduyen07/)
- [thuduyen07-LinkedIn](https://www.linkedin.com/in/thuduyen07/)
- [thuduyen07-Facebook](https://www.facebook.com/thuduyen07) 

# Git

## Dùng git cho dự án đang làm
1. Tạo thư mục tên folder-name ở local
2. `cd folder-name` để vào thư mục vừa tạo
3. Gọi `git clone <link>` để clone repo về local
4. `git status` để kiểm tra repo
5. `git branch` để hiển thị tất cả các nhánh có trong repo
6. `git branch new-branch-name` để tạo nhánh mới
7. `git checkout branch-name` để chuyển nhánh
8. `git add file-name` để thêm file vào staging area 
9. `git commit -m “message”` để thêm các thay đổi ở staging area vào git repo
10. `git push origin branch-name` để đẩy thay đổi lên server

### Note:

- Nhớ pull code mỗi ngày, hoặc trước khi làm việc để tránh trường hợp out updated.
- Nhớ chạy lệnh `mvn clean compile` ngay khi pull code về để tạo pojo, tránh lỗi import bị outdated.
- Nhớ kiểm tra các sensitive data trước khi add và commit
- Dùng `git diff` để xem các thay đổi
- Dùng `git --no-pager log > log-file-name.txt` để xuất nội dung git commit
- Dùng `git --no-pager pull > log-file-name.txt` để xuất nội dung git pull


### Reference:
#### Git Pages
- [Github Pages](https://docs.github.com/en/pages/quickstart)
- [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [documentation](https://docs.github.com/categories/github-pages-basics/)
- [contact support](https://support.github.com/contact)
