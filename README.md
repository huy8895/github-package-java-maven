# github-package-java-maven
demo github package java maven , github action, cicd

---
# 

1. thêm cấu hình vào file pom.xml
```xml
<distributionManagement>
    <repository>
      <id>github</id>
      <name>GitHub Apache Maven Packages</name>
      <url>https://maven.pkg.github.com/huy8895/github-package-java-maven</url>
    </repository>
  </distributionManagement>
```

2. cấu hình cicd như file [file](.github/workflows/github-package.yml)

3. cách sử dụng:
- tạo 1 release giả sử 1.0.0
- tại project cần sử dụng sẽ thêm cấu hình :
  - jitpack:
```xml
<project>
  <repositories>
    <repository>
      <id>jitpack.io</id>
      <url>https://jitpack.io</url>
    </repository>
  </repositories>

  <dependencies>
    <dependency>
      <groupId>com.github.huy8895</groupId>
      <artifactId>github-package-java-maven</artifactId>
      <version>1.0.0</version>
    </dependency>
  </dependencies>
</project>

```
 
- `1.0.0` là tên của bản release.
- nếu code của package được update thì chỉ cần cập nhật version của dependency là được.
