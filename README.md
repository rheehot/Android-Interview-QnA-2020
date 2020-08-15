# Android-Interview-QnA
2021~ 안드로이드 취직 대비 면접 예상 질문들 모음집

> ~~목표: 1일1커밋~~

> 목표 : 1일1커밋 (2020.08.15. 재시작)

-----

# 2020.08.15.
# 안드로이드 `Life-Cycle`에 대하여 설명하시오
> goto [Programming-Study](https://github.com/sungbin5304/Programming-Study#%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0)

사용자가 앱을 `탐색하고`, `나가고`, `다시 들어올 때` 등등의 **상태 변화**에 따라서 이를 앱에서 알아차릴 수 있게 제공하는 `Callback`.

## Application

## Activity
1. `onCreate` : `Activity`가 생성될 때 호출되며 사용자 `interface` 초기화에 사용된다.
2. `onStart` : `Activity`가 멈췄다가 다시 시작되기 **바로 전**에 호출된다.
3. `onResume` : `Activity`가 사용자와 상호 작용하기 **바로 전**에 호출된다.
4. `onPause` : 다른 `Activity`가 보여질 때 호출된다.
5. `onStop` : `Activity`가 더 이상 보여지지 않을 떄 호출된다.
> 이는 메모리가 부족하여 종료될 시에는 호출되지 **않을** 수 있다.<br/>
> 또한 이는 **다른 `Activity`들의 생명주기 작업이 끝나야 호출**된다.
6. `onDestroy` : `Activity`가 소멸될 때(`finish()`) 호출된다.

## Fragment

## 앱 사용 도중에 카카오톡으로 부터 알림이 오면, 사용중인 앱의 `TopActivity`의 생명주기 상태는 어떻게 되나요?

## `onRestart`는 언제 호출되나요?

## `onCreate`와 `onStart`의 차이점은 무엇인가요?

## `onPause`와 `onStop`없이 `onDestory`가 호출되기 위한 조건이 무엇인가요?

# `ViewHolder` 패턴에 대하여 설명하시오

# `Intent`에 대하여 설명하시오

# `Call by Value`와 `Call by Reference`에 대하여 설명하시오

## `Java`는 `CbV`와 `CbR`중 어떤것인지 설명하시오

# 안드로이드 4대 컴포너트에 대하여 설명하시오
> goto [Programming-Study](https://github.com/sungbin5304/Programming-Study#4%EB%8C%80-%EC%BB%B4%ED%8F%AC%EB%84%88%ED%8A%B8)

# `Manifest`에 대해 설명하시오

# `Inflation`에 대해 설명하시오

# `JVM`/`DVM`에 대해 설명하시오

## `Android`는 `JVM`과 `DVM`중 어느것인지 설명하시오

# 안드로이드 `Task`에 대하여 설명하시오

# `Restfull API`에 대하여 설명하시오

# `Looper`에 대하여 설명하시오

# `Wrapper`에 대하여 설명하시오

# `Thread`간 통신 방법에 대하여 설명하시오

# `Intent`의 `Flag`들에 대하여 설명하시오

# 안드로이드의 메모리 관리에 대하여 설명하시오

# 안드로이드의 메모리 구조에 대하여 설명하시오

# `Pending Intent`에 대하여 설명하시오

# `Activity`간 통신에 대하여 설명하시오

# `FCM`의 원리에 대하여 설명하시오

# `ABI`에 대하여 설명하시오

# `HTTP` 라이브러리들의 역사에 대하여 설명하시오
2009년 : `Android` 발표, `HttpClient`, 아파치의 `DefaultHttpClient` 사용<br/>
2011년 : `Google Developer` 블로그에서 `HttpUrlConnection` 사용 권장<br/>
이후 : `Volley`나 `OkHttp`의 등장으로 `HTTP` 통신이 쉬워짐<br/>
2014년 : `HttpClient`가 `Deprecated`되면서 이를 베이스로 하는 `Volley`도 같이 `Deprecated`됨<br/>
이후 : `OkHttp`와 그 래퍼인 `Retrofit`이 등장하여 인기를 가짐<br/>

## `Retrofit`가 인기를 받게된 이유?
`Client` 부분과 `Callback` 형식들을 플러그로 설정 할 수 있다

# `Context`에 대하여 설명하시오
> goto [Programming-Study](https://github.com/sungbin5304/Programming-Study#context)

## `Application Context`

## `Activity Context`

# `Build Process`에 대하여 설명하시오

# `Build Type`에 대하여 설명하시오

# `LMK`에 대하여 설명하시오

## 목적

## Priority

## `OOM KILLER`와의 차이점

-----

# `Issue`를 통한 오타/오류 지적 환영합니다 :)
## 잘 보셨다면, 스타와 포크 부탁드려요!
### 면접 합격 기원합니다.
