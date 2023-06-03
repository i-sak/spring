# Spring boot restapp

### start
![start](./image/start.png)

### Spring-WebMVC 에서 RESTful 지원
아래 3개 Annotation 사용
- @Controller
- @RequestMapping(value="url",method=POST/GET/DELETE/PUT)
- @ResponseBody

```java
@Controller
public class IndexController {

    @RequestMapping(value = "/", method = RequestMethod.GET)
    @ResponseBody
    public String index() {
        return "Hello, Boot";
    }
}
```

### Spring Boot 에서의 RESTful 지원
아래 2개 Annotation 사용
- @RestController
- @X-Mapping 사용

```java
@RestController
public class IndexController {
    @GetMapping("/")
    public String index() {
        return "Hello, Boot";
    }
}
```
@RestController 내부에 @Controller, @ResponseBody 가 포함되어 있다.
@GetMapping 내부에는 @RequestMapping(value="/", method = RequestMethod.GET) 이 포함되어 있다.
