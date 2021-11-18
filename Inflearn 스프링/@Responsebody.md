## @Responsebody

@ResponseBody 가 붙은 파라미터에는 HTTP 요청의 분문 body 부분이 그대로 전달된다.



```java
@GetMapping("hello-string")
@ResponseBody
public String helloString(@RequestParam("name") String name) {
	return "hello " + name;
}
```

예를 들어

localhost:8080/hello-string?name=spring!!!

을 링크에 입력하고

우클릭 -> 페이지 소스를 보면

html 코드가 나오는게 아니라

return 값인 "hello " + name; 인

hello spring!!! 이 출력된다.