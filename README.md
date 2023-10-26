
---

## 혼자 공부하는 컴퓨터구조 + 운영체제 

#

### [Chapter 01] 컴퓨터 구조를 알아야 하는 이유 <br/>

1. 컴퓨터 구조를 배우는 내용은 결국 성능, 용량, 비용과 직결되기 때문입니다.
2. 컴퓨터 구조를 이해하면 입력과 출력에만 집중하는 개발을 넘어 성능, 용량, 비용까지 고려하며 개발하는 개발자가 될 수 있습니다.
3. 컴퓨터는 0과 1로만 표현된 정보만을 이해합니다. 이러한 정보에는 크게 두 종류, 바로 **데이터**와 **명령어**가 있습니다
4. 컴퓨터가 이해하는 숫자, 문자, 이미지, 동영상과 같은 정적인 정보를 가리켜 데이터라고 합니다.
5. 데이터는 명령어 없이는 아무것도 할 수 없는 정보 덩어리입니다. 바로 명령어가 데이터를 움직이고 컴퓨터를 작동시킵니다.
6. 컴퓨터 핵심부품은 중앙처리장치(CPU), 주기억장치(메모리), 보조기억장치, 입출력장치입니다.
7. 메모리는 현재 실행되는 프로그램의 명령어와 데이터를 저장하는 부품입니다. 다시말해 프로그램이 실행되려면 반드시 메모리에 저장되어 있어야합니다.
8. 이때 메모리 속 명령어와 데이터가 중구난방으로 저장되어 있으면 안됩니다. 저장된 명령어와 데이터의 위치는 정돈되어 있어야 합니다. 그래서 **주소**라는 개념이 사용됩니다.
9. 컴퓨터는 주소를 통해 메모리 내에서 원하는 위치로 접근할 수 있습니다.
10. CPU는 컴퓨터의 두뇌입니다. CPU는 메모리에 저장된 명령어를 읽어들이고, 읽어들인 명령어를 해석하고 실행하는 부품입니다.
11. CPU 내부 구성요소 중 가장 중요한 세 가지는 산술논리연산장치(ALU), 레지스터, 제어장치 입니다.
12. ALU는 쉽게 말해 계산기입니다. 컴퓨터 내부에서 수행되는 대부분의 계산은 ALU가 도맡아 합니다.
13. 레지스터는 CPU내부의 작은 임시 저장 장치입니다. 프로그램 실행하는 데 필요한 값들은 임시로 저장합니다. CPU안에는 여러 개 레지스터가 존재하고 각기 다른 이름과 역할을 가집니다.
14. 제어장치는 제어신호라는 전기신호를 내보내고 명령어를 해석하는 장치입니다. (제어신호 크게 두가지 -> 메모리 읽기 / 메모리 쓰기)
15. 보조기억장치는 전원이 꺼져도 보관될 프로그래을 저장하는 부품입니다.
16. 메모리가 현재 실행되는 프로그램을 저장한다면 보조기억장치는 보관할 프로그램을 저장한다고 생각해도 좋습니다.
17. 컴퓨터의 핵심 부품들은 메인보드라는 판에 연결됩니다.
18. 메인보드에 연결된 부품들은 서로 정보를 주고 받을 수 있는데 이는 메인보드 내부에 버스라는 통로가 있기 때문입니다.
19. 시스템버스는 컴퓨터의 네가지 핵심부품(CPU, 메모리 || 보조기억장치, 입출력장치)이 서로 정보를 주고받는 통로입니다.
20. 시스템 버스는 주소 버스, 데이터 버스, 제어버스로 구성되어 있습니다.
 
---

#

### [Chapter 02] 데이터 <br/>

1. 컴퓨터가 이해하는 가장 작은 정보단위를 비트(0,1)라고 합니다.
2. 워드란 CPU가 한 번에 처리할 수 있는 데이터 크기를 의미합니다. 만약 CPU가 한 번에 16비트를 처리할 수 있다면 1워드는 16비트가 됩니다.
3. 0과 1만으로 음수를 표현하는 방법 중 가장 널리 사용되는 방법은 2의보수를 구해 이 값을 음수로 간주하는 방법입니다.
4. 2의 보수를 매우 쉽게 표현하자면 모든 0과 1을 뒤집고 거기에 1을 더한 값으로 이해하면 됩니다.
5. 실제로 이진수만 봐서는 음수인지 양수인지 구분하기 어렵습니다. 그래서 컴퓨터 내부에서 어떤 수를 다룰 때는 이수가 양수인지 음수인지 구분을 위해 플래그를 사용합니다.
6. 십육진법을 사용하는 주된 이유 중 하나는 이진수를 십육진수로, 십육진수를 이진수로 변환하기 쉽기 때문입니다.
7. 컴퓨터가 인식하고 표현할 수 있는 문자의 모음을 문자집합이라고 합니다.
8. 문자집합에 속한 문자라고 해서 컴퓨터가 그대로 이해할 수 있는 건 아닙니다. 문자를 0과 1로 변환해야 비로소 컴퓨터가 이해할 수 있습니다. 이 변환 과정을 문자인코딩이라 하고 이 과정을 거쳐야 0과1로 결과값이 나옵니다.
9. 반대로 0과1을 사람이 이해할 수 있는 문자로 변환하는 과정은 문자 디코딩이라고 합니다.
10. 영어 인코딩과 다르게 한글 인코딩에는 두가지 방식, 완성형(한글 완성형 인코딩)과 조합형(한글 조합형 인코딩)이 존재합니다.
11. 완성형 인코딩 방식은 초성, 중성, 종성의 조합으로 이루어진 완성된 하나의 글자에 고유한 코드를 부여하는 방식입니다 (가 = 1, 나 = 2 ...)
12. 조합형 인코딩은 초성을 위한 비트열, 중성을 위한 비트열, 종성을 위한 비트열을 할당하는 방법입니다.
13. EUC-KR은 대표적인 완성형 인코딩 방식입니다.
14. 유니코드는 EUC_KR보다 훨씬 다양한 한글을 포함하며 대부분 나라의 문자, 특수문자, 화살표나 이모티콘까지 코드로 표현할 수 있는 통일된 문자집합입니다.
15. 유니코드 또한 완성형입니다. 하지만 EUC-KR과 다르게 글자에 부여된 값 자체를 인코딩 값으로 삼지않고 UTF-8, UTF-16, UTF-32 등 다양한 방식으로 인코딩합니다.
  
---

#

### [Chapter 03] 명령어 <br/>
