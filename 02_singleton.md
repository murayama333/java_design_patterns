# デザインパターン - Singletonパターン

次のクラス、インタフェースがあります。

+ SingletonCounter
+ Main

<img src="https://s3-ap-northeast-1.amazonaws.com/optext/java/oop/singleton.png" width="500px" >

Singletonとは単独という意味の言葉です。SingletonCounterは、自身のインスタンスを一つしか生成することができません。

## SingletonCounter

```java
package singleton;

public class SingletonCounter {

	private int max;

	// TODO singleton

	public void countUp() {
		for (int i = 1; i <= max; i++) {
			System.out.println(i);
		}
	}

	public void setMax(int max) {
		this.max = max;
	}
}
```

## Main

```java
package singleton;

public class Main {

	public static void main(String[] args) {

//		SingletonCounter counter1 = new SingletonCounter();
//		SingletonCounter counter2 = new SingletonCounter();

		SingletonCounter counter1 = ???;
		SingletonCounter counter2 = ???;

		counter1.setMax(5);
		counter1.countUp();
		counter2.countUp();
	}
}
```

> counter1もcounter2も同一のインスタンスを参照するようにした。

### 実行結果

```
1
2
3
4
5
1
2
3
4
5
```

## 課題

SingletonCounterクラスのインスタンスを1つしか生成できないようにSingletonCounterクラスを修正してください。またMainクラスでSingletonCounterクラスのインスタンスを生成する処理を実装してください。
