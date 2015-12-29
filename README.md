# Go Programming Language 정리


### package import
	type1 : import (
		    	"fmt"
		    	"math"
			)
	type2 :  import "fmt"
	  		 import "math"


### 함수
	-func 함수명(매개변수명 매개변수타입) 리턴타입 {}
	-func add(x, y int) int {
		return x+y
	} => 두개 이상의 매개변수가 같은 타입일 때 하나만 명시하고 나머지는 생략 가능
	- 하나의 함수는 여러 개의 결과를 반환할 수 있음
	func aaa(x, y int) (int, int) {
		return x, y
	}


### 변수 (Variables)
	- 선언
		var a,b,c int
	  	var aa,bb,cc bool
	- 초기화
		var a,b,c int = 1, 2, 3
		var aa,bb,cc = true, false, "ddd"
	-변수의 짧은 선언
		함수 내에서 := 을 사용하면 var 과 명시적인 타입(e.g. int, bool) 을 생략할 수 있음		


### 상수 (Constants)
	- 상수는 const 키워드와 함께 변수처럼 선언 const Hello = "Hello"
	- 상수는 문자(character), 문자열(string), 부울(bool), 숫자 타입 중의 하나가 될 수 있음


### 반복문 (for)
	- Go 언어는 반복문이 for 밖에 없음
	- 소괄호()가 필요하지 않음, 중괄호{}는 필요함
	- for i := 0; i<10; i++ {}  /  for(i<10) {i++} / for {} <--무한루프


### 조건문 (If)
	- 소괄호()가 필요하지 않음, 중괄호{}는 필요함


### 기본 자료형
	- bool, string, int, int8, int16, int32, int64
	- uint, uint8, uint16, uint32, uint64, uintptr
	- byte (uint8의 다른 이름(alias)), rune (int32의 다른 이름 (alias) 유니코드 코드 포인트 값을 표현합니다.) 
	- float32, float64, complex64, complex128


### 구조체 (Structs)
	- struct는 필드들의 조합임
	- type 선언으로 struct의 이름을 지정할 수 있음
	  	type Vertex struct {
    		X int
    		Y int
		}
	- Vertext.X 로 구조체에 속한 필드에 접근


### 슬라이스 (Slices)
	- 슬라이스는 배열의값을 가리킴
	- p := []int{2, 3, 5, 7, 11, 13}
	- p[1:4] -> [3,5,7] 
	- p[:3] -> [2,3,5]
	- p[4:] -> [11 13]
	- 슬라이스의 zero value는 nil 이다 (var z []int  z는 nil)


### 맵(Maps)
	- 맵은 값에 키를 지정
	- 맵은 반드시 사용하기 전에 make를 명시해야함. new가 아님
	- make를 수행하지 않은 nil에는 값을 할달할 수 없음
	- delete(map, key) : map에서 해당 key 요소를 지움
	- elem, ok = map[key] : ok의 값은  map에 key가 존재한다면 true, 아니면 flase elem은 타입에 따라 0(zero value)


### 스위치 (Switch)
	- case코드를 마치면 알아서 break한다.
	- fallthrough 로 긑나는 case는 스스로 break를 하지 않는다.

# 참고사이트
	[A Tour of Go 한글](http://go-tour-kr.appspot.com/)