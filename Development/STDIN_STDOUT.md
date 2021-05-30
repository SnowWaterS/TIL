# STDIN / STDOUT

Category: Basic
Date: May 30, 2021
Tags: Java, Kotlin

## Java

### STDIN

```java
Scanner scanner = new Scanner(System.in);
int intVal = scanner.nextInt();
int doubleVal = scanner.nextDouble();
String stringVal1 = scanner.next();
scanner.nextLine();
String stringVal2 = scanner.nextLine();
scanner.close();
```

- Scanner 를 통해 입력 받을 수 있다.
- 입력 받는 값의 Type 이 정해져있다면, nextInt(), nextDouble(), next()등을 이용해서 입력 받으면 된다.
    - 이 함수들의 경우, 연속된만큼 type 에 대해 읽으며 빈칸(" ")이나 마지막 개행문자("\n")를 입력받지 않는다.
    - 이후, 바로 nextLine()을 하면 그 라인의 마지막 개행문자까지("\n")을 입력받는다. (바로 엔터를 눌렀다면 개행문자까지("\n")만 입력받는다.)
- nextLine()은 개행문자를 포함하여 한 줄을 읽는다.

### STDOUT

```java
System.out.println("/** Something you want to print **/");    // 개행문자("\n") 포함
System.out.printf("%s", "문자열");                              // 개행문자("\n") 미포함
System.out.printf("%-15s", "문자열");                           // 오른쪽 패딩
System.out.printf("%15s", "문자열");                            // 왼쪽 패딩
System.out.printf("%5d", "123");                              // 0 패딩해서 5자리로 출력
System.out.printf("%.3f", "3.141592");                        // 소수점 3자리
```

- 그 외의 format string
    - `%n` , `\n`: 줄바꿈
    - `%s` : String 형식으로 출력
    - `%d` : integer 형식으로 출력
    - `%f` : float 형식으로 출력
    - `%t` : date, time 형식으로 출력
    - `%o` : 8진수 integer 형식으로 출력
    - `%x` : 16진수 integer 형식으로 출력
    - `%b` : boolean 형식으로 출력
    - `%e` : 지수 형식으로 출력

## Kotlin

### STDIN

```kotlin
val stringVal = readLine()

or

import java.util.Scanner

  val input = Scanner(System.`in`)  
  val a = input.nextInt()  
  val b = input.nextInt()
  input.nextLine()
  val c = input.nextInt()
```

- readLine()을 이용하거나 (null 체크 필요!), `import java.util.Scanner` 하여 Scanner를 이용한다.

### STDOUT

```kotlin
print("문자열")                                // 개행문자("\n") 미포함
println("문자열")                              // 개행문자("\n") 포함
println("%15s".format("문자열"))               // 오른쪽 패딩
println("%.3f".format(3.141592))             // 소수점 3자리
.
.
.
```