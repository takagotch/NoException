### noexception
---
https://noexception.machinezoo.com/

https://github.com/robertvazan/noexception

```java
System.out.println(Exceptions.log().get(() -> "test".substring(5)).orElse("fallback"));

Logger logger = LoggerFactory.getLogger(...);
String result;
try {
  result = "test".substring(5);
} catch (Throwable exception) {
  logger.error("Caught exception", exception);
  result = "fallback";
}
System.out.println(result);

public class ExceptionPolicy {
  public static CheckedExceptionHandler wrap(String message) {
    return Exceptions.wrap(e -> new RuntimeException(message, e));
  }
}
ExceptionPolicy.wrap("Failed to save the upload").run(() -> Files.write(path, data));
```

```
```

```
```


