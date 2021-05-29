# Nest Movie API

## 목적

Nest.js의 구조와 사용 방법 이해한다.

## Nest.js?

> Nest (NestJS) is a framework for building efficient, scalable Node.js server-side applications. It uses progressive JavaScript, is built with and fully supports TypeScript (yet still enables developers to code in pure JavaScript) and combines elements of OOP (Object Oriented Programming), FP (Functional Programming), and FRP (Functional Reactive Programming).

기존 Node.js를 구조화시킨 프레임워크로 TypeScrirpt, OOP, FRP, FP의 요소들을 결합하여 사용한다.

## Decorator

새 함수를 반환하여 전달 된 함수 또는 메서드의 동작을 수정하는 함수이다.
Nest.js에서는 `@decorator()` 이와 같은 형식으로 사용된다.

## Nest.js 구조

`module - controller - provider(service)`
Nest.js의 기본적인 구조는 위와 같다.

### Module

> A module is a class annotated with a @Module() decorator. The @Module() decorator provides metadata that Nest makes use of to organize the application structure.

모듈은 클래스와 같다고 볼 수 있으며, 프로그램 구조를 구성하는데 사용하는 메타데이터를 제공한다.

### Controller

> Controllers are responsible for handling incoming requests and returning responses to the client.

클라이언트의 request 제어하고 response 하는 부분으로 애플리케이션의 특정 요청을 수신하고 응답한다.

### Service

> Providers are a fundamental concept in Nest. Many of the basic Nest classes may be treated as a provider – services, repositories, factories, helpers, and so on. The main idea of a provider is that it can inject dependencies; this means objects can create various relationships with each other, and the function of "wiring up" instances of objects can largely be delegated to the Nest runtime system.

비즈니스 로직를 담는 부분이며 Nest.js에서 주요 개념은 DI(의존성 주입)이라는 패턴이다.

#### 의존성 주입

[블로그 작성](https://blog.naver.com/dilrong/222373919928)

### DTO & Validation

Data Transfer Object 정보를 교환하는데 타입을 체크하기 위한 스키마이다.
DTO는 값을 검증만 하고 처리는 하지 않는다.
그래서 Class Validation를 이용하여 검증에 대한 처리를 할 수 있다.

```
npm i --save class-validator class-transformer
```

## 참고

[Nest.js Docs](https://docs.nestjs.com/)
[NomadCoders Nest.js](https://docs.nestjs.com/)
[자바스크립트 데코레이터 이해하기](https://ui.toast.com/weekly-pick/ko_20200102)
