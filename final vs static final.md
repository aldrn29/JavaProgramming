## final
'변경할 수 없는, 최종적'이란 뜻을 가진 final!

> final 키워드는 필드, 메소드, 클래스에서 쓸 수 있는데 그 중 final 필드는 최종적으로 변경할 수 없는 즉, 수정할 수 없음을 의미한다. 그렇다면 final 필드와 static final 필드는 무슨 차이가 있을까?

## flnal vs static final 
#### final 필드는 상수일까?
static final로 선언해주어야 상수가 된다. 상수란 변하지 않는 값을 의미하는데 물론 final로 선언된 값도 변하지 않지만, 선언할 때마다 객체에 저장되고 생성자의 매개 값을 통해서 여러가지 값을 가질 수 있기 때문에 상수라고 보기는 어렵다. 즉, 메모리에 여러 번 적재되게 된다. 반면 static final로 선언된 값은 한 번 선언하면 메모리에 적재되며 한 자리만 차지하게 된다.

```
final int a = 2;
static final int b = 2; 
```

#### final
```
Class Test {
  public final int a;
}

Test t1 = new test();
t1.a = 10;
Test t2 = new Test();
t2.a = 20;
``` 

#### static final
```
Class StaticTest {
  public static final int a;
}

Test t1 = new Test();
t1.a = 10;
Test t2 = new Test();
t2.a = 20;  → Error! 이미 첫번째 객체 생성이 있었기 때문에, 더 이상 값을 등록할 수 없다.
```

