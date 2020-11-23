# Spring-Boot-Jib-With-Harbor

Spring Boot 프로젝트를 [Jib](https://github.com/GoogleContainerTools/jib) 를 이용해 Container 화 하고 Harbor 에 배포해보는 예제 프로젝트

## Requirement

이 예제를 실행하기 위해서는 Harbor 가 필요합니다. 없을 시 [링크](https://github.com/lutics/Harbor-On-GCP)를 참고하여 준비

## Command Line

일반적으로 gcr.io 나 기타 보유중인 Repository 가 있다면 `build.gradle` 수정하고 아래의 명령어로 배포가 가능하다

```
./gradlew jib
```

위 링크를 이용한 Harbor 프로젝트와의 연계를 위해서는 `-DsendCredentialsOverHttp=true` 값을 추가해야한다

```
./gradlew jib --image=34.70.211.125:80/library/sample -DsendCredentialsOverHttp=true
```
