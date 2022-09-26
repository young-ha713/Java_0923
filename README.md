# Java_0923  
  
  
  
  
  
  
  
![아침문제](https://user-images.githubusercontent.com/80766275/192189897-f0cfb5e8-801b-4091-a1df-a1ed1c622e75.PNG)
  
  
  
-----------------------------------------------------------------------------------------------------------------  
  
  
  
  
인트 타입  
  
```
package TestCode;

public class Ex {

	public static void main(String[] args) {
		
		int a = 20; //객체가 아님  why?주소값저장하는게 아니어서? int 원시변수이기 때문에 값이 그대로 저장됨.객체는 주소값을 가짐
		//선언문 자료형 (참조타입,원시타입) 참조타입은 객체의 주소값
		
		//a =null; //오류 나는 이유는 널은 참조 타입에만 가능
		a = a +30;
		System.out.println(a);
		Integer b = 20; //는 객체
		b = b+40;
		System.out.println(b);
		b = a + b;
		System.out.println(b);
		a =a+b;
		System.out.println(a);
		b = null;
		System.out.println(b);
		
		if(b==null) {
			b=0;
		} //널값 가질 수 있다. 왜 ?객체타입이기 때문에
		
		
		//자바에서 자료형은 객체로 제공.int같은 겨우는 원시타입처럼 사용하는것이 주된 사용
		//그래서 자바에서는 Integer라는 클래스를 int 처럼 사용 할 수 있게 해준다.
		//두 개의 자료형의 가장 큰 차이는 객체 타입과 원시타입이라는 것이고 객체 타입의 인티저는 널값을 가질 수 있다.
		//가끔씩은 대입될 자료가 null일 경우가 있다.이를 방지하기 위해서는 Integer로 선언하는것이다.
		
	}

}
```  
  
  
  
  
### 접근제어자    
  
클래스 기준으로 먼저 생각해서 자신의 클래스 자원(전역변수,메서드)을 외부에서 참조변수로 사용할때의 권한을 부여..  
  
외부라고 함은 같은 클래스, 같은 패키지의 다른클래스,다른 패키지의 다른클래스 이렇게 3개로 분류하여 생각 할 수 있다.  
  
  
종류 - private, public, default, protected  
  
private는 오직 같은 클래스 내에서만 접근 가능  
default는 private성격을 포함하며 같은 패키지 다른 클래스에서만 접근 가능,다른 패키지는 접근 불가  
public모두 가능 ,, 단 프로젝트가 다르면 불가 .프로젝트가 다르면 전혀 다른 프로그램임  
  
  
  
객체 지향에 어울리게 작성하는 방법은 일단 모두 private로 해 놓고,외부에서 사용해야할때 public으로 열어둠  
단 전역변수는 public 잘 사용하지 않음 메서드만 public으로 많이 지정
  
  
![image](https://user-images.githubusercontent.com/80766275/192201550-e7130140-f7e1-4cdf-ab65-1a9a1cfad1a9.png)
  
  
![image](https://user-images.githubusercontent.com/80766275/192203931-4f57381e-163b-4027-9b1b-83f447f0aacf.png)
프라이빗으로 막혀있기 때문에 메소드를 새로 생성해 멤버에서 접근시 다른 방법으로 접근해야 한다..!  
  
  
![image](https://user-images.githubusercontent.com/80766275/192204659-53cea504-d300-493d-9608-b3ec6254c2b4.png)

  
  
![image](https://user-images.githubusercontent.com/80766275/192205316-e6003f87-132c-49d3-8c07-d1928b29104d.png)
  
  
----------------------------------------  
객체지향 언어에서는 객체를 만들고 여러 클래스에서 이를 사용한다(재사용성)  
객체는 전역변수와 메서드로 구성된다  
다른 클랫에서 특정 객체의 자원을 이용할때 이용하려고 하는 대상 클래스는 자신의 전역변수와 메서드를 외부에 노출시키지 않아야 한다.  
물론 공용으로 사용한다면 노출해도 되지만 보안상 노출하지 않는것이 좋다  
  
그런데 외부에서 전역변수나 메서드자원이 필요하다면 자원을 리턴해줘야 프로그램이 정상동작한다  
그래서 접근제어자로 그범위를 지정하고 되도록 전역변수가 아닌, 메서드로 해당 자원을 리턴해준다  
  
즉 전역변수 자원 노출 금지 .적합한 접근제어자가 private  
  
  
  
--------------------------------------------------
  
  
![image](https://user-images.githubusercontent.com/80766275/192226378-daaeb561-ab1f-4ec5-8b35-2ac1a022af8a.png)
  



  
  
