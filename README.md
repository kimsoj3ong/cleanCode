### 2.의도를 분명히 하라

```java
// 변경 전
Optional<User> u = userRepository.findById(id);

// 변경 후
Optional<User> userInfo = userRepository.findById(userId);
```

### 3.그릇된 정보와 혼동을 피하라

```java
// 변경 전
Optional<User> userInfoList = userRepository.findById(userId);

// 변경 후
Optional<User> userInfo = userRepository.findById(userId);
```

### 4.의미 있게 구분하고 일관된 어휘를 유지하라

```java
// 변경 전
userService.insertUserList(user);
userService.addUserInfo(user);

// 변경 후
userService.updateUserList(user);
userService.updateUserInfo(user);
```

### 5.발음하기 쉽고 검색이 가능한 이름을 써라

```java
// 변경 전
Date d = new Date();

// 변경 후
Date currentDate = new Date();
```

### 6.인코딩과 불필요한 접두어를 피하라

```java
// 변경 전
String m_strEmail = "kimsojeong102@gmail.com";

// 변경 후
String email = "kimsojeong102@gmail.com";
```

### 7.명사와 동사의 구분
```java
// 변경 전
public void user() { ... }

// 변경 후
public void updateUserInfo() { ... }
```

### 8.맥락을 부여하고 불필요한 맥락은 제거하라
```java
// 변경 전
private String userAddressCity;
private String userAddressZip;

// 변경 후
class Address {
    private String city;
    private String zipCode;
}
```

### 9.기발함보다 명료함을 택하라
```java
// 변경 전
updateUserInfo(youngForty);

// 변경 후
updateUserInfo(userInfo);
```

### 10.해법 영역과 문제 영역의 균형
```java
// 변경 전
public class jobQueueProcessor { ... }

// 변경 후
public class paymentApprovalProcessor  { ... }
```




