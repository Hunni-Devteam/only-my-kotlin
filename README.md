# only-my-kotlin

You might be think about railgun ... blahblah.

## If - When statement

... 를 사용해 Switch 문과 유사하게 사용할 수 있음
결과를 변수에 할당하거나, 함수의 리턴으로 바로 사용하거나, 심지어 `is Type` 형태로 타입 체크도 가능함

ex)
```kotlin
fun Request.getBody() =
  when (val response = executeRequest()) {
    is Success -> response.body
    is HttpError -> throw HttpException(response.status)
  }

```
