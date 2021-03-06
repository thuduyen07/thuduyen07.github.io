## Welcome to thuduyen07 GitHub Pages

You can also check out my social medias: 
- [thuduyen07-Github](https://github.com/thuduyen07/)
- [thuduyen07-LinkedIn](https://www.linkedin.com/in/thuduyen07/)
- [thuduyen07-Facebook](https://www.facebook.com/thuduyen07) 
- [thuduyen07-topcv](https://www.topcv.vn/xem-cv/UlsAVlUCDwkFVQEIA1EIUlcEUVNRBANRBQ4HWwc662)

# Git

### Dùng git cho dự án đang làm
1. Tạo thư mục tên `duyen-folder` ở local
2. `cd duyen-folder` để vào thư mục vừa tạo
3. Gọi `git clone <link>` để clone repo về local
4. `git status` để kiểm tra repo
5. `git branch` để hiển thị tất cả các nhánh có trong repo ở local
6. `git branch duyen-branch` để tạo nhánh mới
7. `git checkout duyen-branch` để chuyển nhánh
8. `git add duyen-file` để thêm file vào staging area 
9. `git commit -m “message”` để thêm các thay đổi ở staging area vào git repo
10. `git checkout master` và `git pull` để cập nhật thay đổi mới nhất
11. `git checkout duyen-branch` để về lại nhánh đang làm việc
12. `git merge master` để kiểm tra và resolve conflict nếu có --> commit code update
13. `git push origin duyen-branch` để đẩy thay đổi lên server

### Note:
- Nhớ pull code mỗi ngày, hoặc trước khi làm việc để tránh trường hợp out updated.
- Nhớ chạy lệnh `mvn clean compile` ngay khi pull code về để tạo pojo, tránh lỗi import bị outdated.
- Nhớ kiểm tra các sensitive data trước khi add và commit
- Dùng `git stash save "mesage"` và `git stash pop` để hotfix
- Dùng `git diff` để xem các thay đổi
- Dùng `git --no-pager log > log-file-name.txt` để xuất nội dung git commit
- Dùng `git --no-pager pull > log-file-name.txt` để xuất nội dung git pull
- Sửa commit message: 
    1. Sửa cái gần nhất: `git commit --amend -m "meomeo new message"`
    2. Sửa cái xa xa =))
    - Dùng `git rebase -i HEAD~commit-number` để mở file
    - Đổi `pick` thành `reword` ở commit muốn sửa
    - Sửa và lưu file
    - *Note: Nhớ kiểm tra branch trước khi tiếp tục các bước tiếp theo =))*
    - Ref. [How to Change Commit Message in Git (w3docs.com)](https://www.w3docs.com/snippets/git/how-to-change-commit-message.html)
    
# Allure report
*Note: All information in this article is used for Windows.*

Allure framework is a test report tool.

### Install

Using Power Shell

- Install: `scoop install allure`
- Update: `scoop update allure`
- Check installation: `allure --version`

### Test execution

Configuration:

1. In `allure.properties` (in `src/test/resource`)
    
    ```
    allure.results.directory=target/allure-results
    allure.link.issue.pattern=https://example.org/browse/{}
    allure.link.tms.pattern=https://example.org/browse/{}
    ```
    
    Note:
    
    - `allure.link.my-link-type.pattern=https://example.org/custom/{}/path` specify the link pattern for `@TmsLink`, allure will replace `{}` placeholders with value specified in annotation
2. In `pom.xml` (setting system properties)

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-surefire-plugin</artifactId>
            <version>2.20</version>
            <configuration>
                <systemPropertyVariables>
                    <allure.results.directory>${project.build.directory}/allure-results</allure.results.directory>
                    <allure.link.issue.pattern>https://example.org/browse/{}</allure.link.issue.pattern>
                    <allure.link.tms.pattern>https://example.org/browse/{}</allure.link.tms.pattern>
                </systemPropertyVariables>
            </configuration>
        </plugin>
    </plugins>
</build>
```

### Report generation

`allure serve <allure-result-path>`

Clean report: `allure report clean` (by default: looking for the report in **allure-results**
 folder)

- **Environment**
    
    add `environment.properties` to `allure-results` before generating report
    
    ```xml
    Browser=Chrome
    Browser.Version=98.0.4758.102  //todo get version automatically
    Stand=Production
    ```
    
- **Categories**
    
    Custom defects classification by adding `allure-results/categories.json` hoặc `test/resource/categories.json`
    
    ```json
    [
    {
    	"name": "Problems",
    	"matchedStatuses": ["passes", "slipped", "unknown", "broken", "failed"],
    	"messageRegex": ".*gau-gau.*",
    	"traceRegex": ".*FileNotFoundExceptions.*"
      }
    ]
    ```
    

### Note

1. surefire maven-plugin: create report automatically
2. How to use `@TmsLink` and `@Issue`, configure in `allure.properties`
3. Using `@Flaky`for flaky tests, which are not always passed or failed, they fail from time to time

### Questions

1. Get chrome version automatically for `environment.propreties`?

### Reference

[Allure Framework (qameta.io)](https://docs.qameta.io/allure/)

# Log4j


### Git Pages reference
- [Github Pages](https://docs.github.com/en/pages/quickstart)
- [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [documentation](https://docs.github.com/categories/github-pages-basics/)
- [contact support](https://support.github.com/contact)
