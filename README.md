# Android-Interview-QnA
2021~ 안드로이드 취직 대비 면접 예상 질문들 모음집

> ~~목표: 1일1커밋~~

> 목표 : 1일1커밋 (2020.08.15. 재시작)

-----

# 2020.08.15.
# 안드로이드 `Life-Cycle`에 대하여 설명하시오
> goto [Programming-Study](https://github.com/sungbin5304/Programming-Study#%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0)

사용자가 앱을 `탐색하고`, `나가고`, `다시 들어올 때` 등등의 **상태 변화**에 따라서 이를 앱에서 알아차릴 수 있게 제공하는 `Callback`.

## ~~Application~~
> 분명 어디선가 `Application`도 생명주가가 있다고 봤는데, 찾아보니깐 정보가 없다.<br/>
> ~~일단 보류~~

## Activity
1. `onCreate` : `Activity`가 생성될 때 호출되며 사용자 `interface` 초기화에 사용됨
2. `onStart` : `Activity`가 멈췄다가 다시 시작되기 **바로 전**에 호출됨
3. `onResume` : `Activity`가 사용자와 상호 작용하기 **바로 전**에 호출됨
> **다른 `Activity`가 `ForeGround`로 보여질 때 호출됨**
4. `onPause` : 다른 `Activity`가 보여질 때 호출됨
> **다른 `Activity`가 `BackGround`로 보여질 때 호출됨**
5. `onStop` : `Activity`가 더 이상 보여지지 않을 떄 호출됨
> 이는 메모리가 부족하여 종료될 시에는 호출되지 **않을** 수 있음<br/>
> 또한 이는 **다른 `Activity`들의 생명주기 작업이 끝나야 호출**됨<br/>
> 그리고 **매우 짧은 호출 유지 시간**을 가짐<br/>
> 마지막으로 `이 상태`에서 `onSaveInstanceState()` 메소드가 호출됨
6. `onDestroy` : `Activity`가 소멸될 때(`finish()`) 호출됨

### `ForeGround`
현재 `Activity` **밖**에서 실행되는 것

### `BackGround`
현재 `Activity` **안**에서 다른 작업과 **동시**에 뒤에서 실행되는 것

## Layout
1. `onAttachedToWindow` : `View`가 `Window`에 연결되면 호출됨
> `Drawing`할 표면이 알고있는 단계 -> `listener` 설정 가능
2. `measure` 
3. `onMeasure` : `View`의 `Size`를 확인하기 위해 호출됨
> `ViewGroup`일 경우 계속해서 `Child View`에 대한 `Size` 측정을 하고, 그에 대한 결과로 자신의 `Size`를 결정
4. `layout`
5. `onLayout` : `View`의 `Size`를 측정하여 `position` 설정 후 호출됨
6. `dispatchToDraw`
7. `draw`
8. `onDraw` : `View`가 그려질 준비가 되었을 때 호출됨
> `onDraw`는 여러번 호출되므로, 여기서는 `Object`를 만들면 안됨

### `onDetechedFromWindow`
`View`가 `Window`에서 분리될 때 호출됨
> 더 이상 `Drawing`할 `View`가 없음을 알림 -> 모든 작업들을 정리해야 하는 시기

### `onFinishInflate`
`View` 전개가 끝난 후 호출됨
> `Layout`일 경우, 모든 `Child View`가 추가 된 후에 호출됨

### `MeasureSpec`
`MeasureSpec`은 `parent`에서 `child`으로 전달되는 `Layout`들의 요구 사항을 캡출화함

#### `MeasureSpec.EXACTLY`
`Parent View`가 `Child View`의 정확한 `Size`를 결정함.
> `Child View`의 `Size`에 관계없이 무조건 정해진 `Size`로 설정함

#### `MeasureSpec.AT_MOST`
`Child View`는 지정된 `Size`까지의 원하는 만큼 `Size`를 정할 수 있음

#### `MeasureSpec.UNSPECIFIED`
`Parent View`가 `Child View`의 `Size`에 대해 제한을 두지 않음
> `Child View`는 원하는 만큼의 `Size`를 정할 수 있음

### `requestLayout()`과 `invalidate()`의 차이점
#### `requestLayout()`
`measure`부터 `Layout`을 재호출

#### `invalidate()`
`dispatchToDraw()`부터 `Layout`을 재호출

## Fragment

## 앱 사용 도중에 카카오톡으로 부터 알림이 오면, 사용중인 앱의 `TopActivity`의 `Life-Cycle` 상태는 어떻게 되나요?

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
`Client` 부분과 `Callback` 형식들을 플러그로 설정 할 수 있음

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

# `**Big** Size Image` 처리 방법

# `Callable`과 `Runnable`의 차이점

-----

# `Issue`를 통한 오타/오류 지적 환영합니다 :)
## 잘 보셨다면, `Star`와 `Fork` 부탁드려요!
### 이 난잡한 `repository`를 보는 분들과 저의 면접 합격을 기원합니다.
