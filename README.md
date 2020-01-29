# 송금 Service Architecture 설계 및 구현

## 개발 환경

- IDE / Intellij
- Repository / github
- CI/CD / Jenkins
    - TEST → Junit
- Gateway Server / Nginx
- WAS & Framework / SpringBoot(Tomcat)
- DB
    - RDB → Mysql
    - In memory → Redis

## 요구 사항

- Frontend는 간단히 HTML&JS 혹은 RestAPI로만 구성
- Springboot는 총 3개
    - Springboot1 → 송금 Domain
    - Springboot2, Springboot3 → 사용자 Domain, Load-balancing
    - 서로 간의 Communication을 위한 방법 고려
    - 전체 Transaction 혹은 각 Communication간의 Timeout 또한 고려해보기
- Failover 설계 & 모든 Thread 죽었을 시 설계
- 부하 테스트 및 여러 테스트 진행 해보기
- TDD(Test-driven Development), DDD(Domain-driven Development) 적용해보기
