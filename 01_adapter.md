# デザインパターン - Adapterパターン

次のクラス、インタフェースがあります。

+ Printable
+ LegacyPrinter
+ Main

<img src="https://s3-ap-northeast-1.amazonaws.com/optext/java/oop/adapter.png" width="500px" >

LegacyPrinterクラスは過去の開発プロジェクトで作成したクラスです。

今回の開発ではMainクラスの中で、Printableインタフェースを使って、LegacyPrinterクラスのインスタンスを扱いたいのですが、PrintableインタフェースとLegacyPrinterクラスには互換性がありません。

## Printable

```java
package adapter;

public interface Printable {

	void print(String line);

}
```

## LegacyPrinter

```java
package adapter;

public class LegacyPrinter {

	public void doPrint(String row){
		System.out.println(row);
	}
}
```

## Main

```java
package adapter;

public class Main {
	public static void main(String[] args) {

		String printData = "Hello World";

		// Printable printer = new LegacyPrinter();
		Printable printer = ???;
		printer.print(printData);
	}
}
```

### 実行結果

```
Hello World
```

## 課題

Mainクラスの???の部分を考えてプログラミングしてください。ただし、Printable、LegacyPrinterを修正してはいけません。新規クラスを作成することでこの問題を処理します。
