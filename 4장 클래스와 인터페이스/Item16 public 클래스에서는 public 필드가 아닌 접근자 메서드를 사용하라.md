### 퇴보한 클래스

```
class Point {
  public double x;
  public double y;
}
```

위와 같은 클래스는 필드에 직접 접근이 가능하기 때문에 정보은닉의 이점을 가질 수 없다.

### 캡슐화된 클래스

```
class Point {
  private double x;
  private double y;

  public Point(double x, double y) {
    this.x = x;
    this.y = y;
  }

  public double getX() { return x; }
  public double getY() { return y; }

  public void setX(double x) { this.x = x; }
  public void setY(double y) { this.y = y; }
}
```

위와 같은 방식으로 getter라는 접근자를 통해 패키지 바깥에서 접근할 수 있도록 한다.

### `package-private 클래스` 혹은 `private 중첩 클래스`를 이용하게 되면 필드를 노출해도 어떠한 문제도 생기지 않는다.

표현하려는 추상 개념만 올바르게 표현해주면 된다. 이 방식은 코드 면에서나 접근자 방식보다 훨씬 깔끔하다.
