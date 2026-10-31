# 내게 맞는 복지 혜택 찾기

복지서비스 정보를 바탕으로 사용자에게 맞는 혜택을 쉽게 안내하는 Spring Boot 웹 애플리케이션의 초기 프로젝트입니다. 현재 애플리케이션 기능과 도메인 구현은 포함하지 않습니다.

## 기술 스택

- Java 21
- Spring Boot 3.5.16
- Spring Web, Spring Data JPA, Thymeleaf, Validation
- MySQL Connector/J
- Gradle (Groovy DSL)

## 실행 환경 설정

JDK 21을 설치하고 프로젝트 루트에서 다음 환경변수를 설정합니다. 데이터베이스 접속 정보는 환경변수로만 관리합니다.

```powershell
$env:DB_HOST = "localhost"
$env:DB_PORT = "3306"
$env:DB_NAME = "welfare"
$env:DB_USERNAME = "your-username"
$env:DB_PASSWORD = "your-password"
```

개발 설정은 기본 활성 프로필 `dev`를 사용합니다. 운영에서는 `SPRING_PROFILES_ACTIVE=prod`를 지정하고 동일한 DB 환경변수를 운영 환경에 안전하게 주입합니다.

```powershell
$env:SPRING_PROFILES_ACTIVE = "dev"
./gradlew.bat bootRun
```

운영 빌드 및 테스트:

```powershell
./gradlew.bat clean build
./gradlew.bat test
```

현재 데이터베이스 이름과 계정은 예시 값으로 설정하지 않았으며 실행 전 실제 환경에 맞는 값을 지정해야 합니다. JPA의 스키마 자동 변경은 비활성화되어 있습니다.
