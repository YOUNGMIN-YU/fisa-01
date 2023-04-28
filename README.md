# fisa01 recap

package step04.exception;


//1. 실습 도중 사용해 본 다중 정의(오버 로딩)가 무엇이 있을까요? 
//2. 그럼 오버라이딩이 뭘까요?
//3. 로컬 변수의 초기화가 불가능하다는 게 어떤 뜻일까요? 예시를 하나 찾아봅시다
//4. 스태틱 함수에서 일반 함수를 호출할 수 없는 이유는 무엇일까요?

```
class Person {
	String name;
	int age;

	public Person() {
	}

	public Person(String name, int age) {
		this.name = name;
		this.age = age;
	}

	public void printInfo() {
		System.out.println(name + " : " + age);
	}
}

class Developer extends Person {
	String language; //자손만의 변수

	Developer() {
	}

	Developer(String name, int age, String language) {
		// this.name = name; // bonus
		// this.age = age; // bonus
		// 5. 위의 직접 입력 말고 부모 클래스의 생성자를 이용해서 name과 age 값을 설정해 주세요

		this.language = language;
	}

	public void printInfo() {
		// super.printInfo(); // 6. 슈퍼를 넣었을 때 출력값과 안 넣었을 때 출력값
		System.out.println("language : " + language);
	}
}

class Test {
	public static void main(String[] args) {
		Developer developer = new Developer("banana", 20, "ko-KO");

		developer.printInfo();

	}
}
```
