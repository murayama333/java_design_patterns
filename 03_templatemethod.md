# デザインパターン - Template Methodパターン

次のクラス、インタフェースがあります。

+ IncrementCounter
+ DecrementCounter
+ Main


<img src="https://s3-ap-northeast-1.amazonaws.com/optext/java/oop/template.png" width="500px" >

IncrementCounter、DecrementCounterクラスは類似したクラスで、前処理（"Start"表示）、後処理（"End"）が共通しています。

## IncrementCounter

```java
package template;

public class IncrementCounter {

	public void count(int max){

		System.out.println("Start");

		for(int i = 1; i <= max; i++){
			System.out.println(i);
		}

		System.out.println("End");
	}

}
```



## DecrementCounter

```java
package template;

public class DecrementCounter {

	public void count(int min){

		System.out.println("Start");

		for(int i = 100; i >= min; i--){
			System.out.println(i);
		}

		System.out.println("End");
	}

}
```

## Main

```java
package template;

public class Main {

	public static void main(String[] args) {
		IncrementCounter inc = new IncrementCounter();
		inc.count(3);

		DecrementCounter dec = new DecrementCounter();
		dec.count(97);
	}
}
```

### 実行結果

```
Start
1
2
3
End
Start
100
99
98
97
End
```

## 課題

IncrementCounter、DecrementCounterクラスの重複するコード（前処理、後処理）を共通化してください。

### 重複 - 前処理

```java
System.out.println("Start");
```

### 重複 - 後処理

```java
System.out.println("end");
```
