***
# 제 1장 데이터 모델링의 이해
> ## 제 1절 데이터 모델의 이해
>> ### 1.모델링의 이해
>>> #### 가.모델링의 정의
>>>> ##### 사람이 살아가면서 접할 수 있는 다양한 현상은 사람, 사물, 개념 등에 의해 발생된다고 했을 때, 모델링은 이것을 표기법에 따라 표기하는 것 자체를 의미한다.
>>> #### 나.모델링의 특징
>>>> ##### '추상화'는 현실세계를 일정한 형식에 맞추어 표현한다는 의미로 정리할 수 있다. 즉 다양한 현상을 일정한 양식인 표기법에 따라 표현하는 것이다.
>>>> ##### '단순화'는 복잡한 현실세계를 약속된 규약에 의해 제한된 표기법이나 언어로 표현하여 쉽게 이해할 수 있도록하는 개념을 의미한다.
>>>> ##### '명확화'는 누구나 이해하기 쉽게 하기 위해 대상에 대한 애매모호함을 제거하고 정확하게 현상을 기술하는 것이다.
>>> #### 다.모델링의 세 가지 관점
>>>> ##### 1) 데이터관점 : 업무가 어떤 데이터와 관련이 있는지 또는 데이터 간의 관계는 무엇인지에 대해서 모델링하는 방법
>>>> ##### 2) 프로세스관점 : 실제하고 있는 업무는 무엇인지 또는 무엇을 해야하는지를 모델링하는 방법
>>>> ##### 3) 데이터와 프로세스의 상관관점 : 업무가 처리하는 일의 방법에 따라 데이터는 어떻게 영향을 받고 있는지 모델링하는 방법
***
>> ### 2.데이터 모델의 기본 개념 이해
>>> #### 가.데이터 모델링의 정의
>>>> ##### 정보시스템을 구축하기 위한 데이터 관점의 업무 분석 기법
>>>> ##### 현실세계의 데이터에 대해 약속된 표기법에 의해 표현하는 기법
>>>> ##### 데이터베이스를 구축하기 위한 분석, 설계의 과정
***
>> ### 3.데이터 모델링의 중요성과 유의점
>>> #### 중요성 : 파급효과, 복잡한 정보 요구 사항의 간결한 표현, 데이터 품질
>>> #### 유의점 : 중복, 비유연성, 비일관성
***
>> ### 4.데이터 모델링의 3단계 진행
>>> #### 1.개념적 데이터 모델링 : 추상화 수준이 높고 업무 중심적이고 포괄적인 수준의 모델링 진행. 전사적 데이터 모델링, EA 수립 시 많이 이용
>>> #### 2.논리적 데이터 모델링 : 시스템으로 구축하고자 하는 업무에 대해 Key, 속성, 관계등을 정확하게 표현, 재사용성이 높음
>>> #### 3.물리적 데이터 모델링 : 실제로 데이터베이스에 이식할 수 있도록 성능, 저장 등 물리적인 성격을 고려하여 설계
***
>> ### 5.프로젝트 생명주기에서 데이터 모델링
>>>> #### 보통 분석 단계에서 업무 중심의 논리적인 데이터 모델링을 수행하고, 설계 단계에서 물리적인 데이터 모델링을 수행한다.
***
>> ### 6.데이터 모델링에서 데이터 독립성의 이해
>>> #### 가.데이터 독립성의 필요성
>>>> ##### 일체적 구성에서 기능화한 구성의 가장 큰 목적은 상호간 영향에서 벗어나 개별 형식이 가지는 고유의 기능을 유지시키고 그 기능을 극대화하기 위함이다.
>>>> ##### 데이터 독립성에는 지속적으로 증가하는 유지보수 비용을 절감, 데이터 복잡도를 낮추며 중복된 데이터를 줄이기 위한 목적이 있다. 또한 끊임없이 나오는 사용자의 요구사항에 대해 화면과 데이터베이스 간에 서로 독립성을 유지하기 위한 목적으로 데이터 독립성 개념이 출현했다고 할 수 있다.
>>> #### 나.데이터베이스 3단계 구조
>>>> ##### 외부 단계, 개념적 단계, 내부적 단계로 구성된 서로 간섭되지 않는다.
>>> #### 다.데이터 독립성 요소
>>>> ##### 외부스키마(External Schema)
>>>>> ##### - 뷰 단계 여러 개의 사용자 관점으로 구성, 즉 개개 사용자 단계로서 개개 사용자가 보는 개인적 DB 스키마
>>>>> ##### - DB의 개개 사용자나 응용 프로그래머가 접근하는 DB 정의
>>>>> ##### - 비고 : 사용자 관점
>>>> ##### 개념스키마(Conceptual Schema)
>>>>> ##### - 개념 단계 하나의 개념적 스키마로 구성 모든 사용자 관점을 통합한 조직전체의 DB를 기술한 것
>>>>> ##### - DB에 저장되는 데이터와 그들 간의 관계를 표현하는 스키마
>>>>> ##### - 비고 : 통합 관점
>>>> ##### - 내부스키마(Internal Schema)
>>>>> ##### - 내부 단계와 내부 스키마로 구성됨. DB가 물리적으로 저장된 형식
>>>>> ##### - 물리적 장치에서 데이터가 실제적으로 저장되는 방법을 표현하는 스키마
>>>>> ##### - 비고 : 물리적 저장구조
>>> #### 라.두 영역의 데이터 독립성
>>>> ##### 논리적 독립성 - 개념 스키마가 변경되어도 외부 스키마에는 영향을 미치지 않도록 지원하는 것
>>>> ##### 물리적 독립성 - 내부 스키마가 변경되어도 외부, 개념 스키마는 영향을 받지 않도록 지원하는 것
>>> #### 마.사상
>>>> ##### 영어 'Mapping'은 우리말로 '사상'이라고 번역된다. 이것은 상호 독립적인 개념을 연결시켜주는 다리를 뜻한다.
>>>> ##### 외부적,개념적 사상(논리적 사상) - 외부적 뷰와 개념적 뷰의 상호 관련성을 정의함
>>>> ##### 개념적,내부적 사상(물리적 사상) - 개념적 뷰와 저장된 데이터베이스의 상호관련성을 정의함
***
>> ### 7.데이터 모델링의 중요한 세 가지 개념
>>> #### 가.데이터 모델링의 세 가지 요소
>>> ##### - 업무가 관련하는 어떤 것(Things)
>>> ##### - 어떤 것이 가지는 성격(Attributes)
>>> ##### - 업무가 관여하는 어떤 것 간의 관계(Relationships)
>>> #### 나.단수와 집합의 명명
>>>> ##### 어떤 것(Thing)
>>>> ##### 복수, 집합 개념 - 엔터티 타입
>>>> ##### 복수, 집합 개념 - 엔터티
>>>> ##### 개별, 단수 개념 - 엔터티
>>>> ##### 개별, 단수 개념 - 인스턴스, 어커런스
>>>> ##### 어떤 것의 간의 연관(Association between Things)
>>>> ##### 복수, 집합 개념 - 관계
>>>> ##### 개별, 단수 개념 - 패어링
>>>> ##### 어떤 것의 성격(Characteristic of a Thing)
>>>> ##### 복수, 집합 개념 - 속성
>>>> ##### 개별, 단수 개념 - 속성값
***
>> ### 8.데이터 모델링의 이해관계자
***
>> ### 9.데이터 모델의 표기법인 ERD 이해
>>> #### 가.ERD 표기법으로 모델링하는 방법
>>>> ##### ERD(Entity Relationship Diagram)는 각 업무 분석에서 도출된 엔터티와 엔터티간의 관계를 이해하기 쉽게 도식화된 다이어그램으로 표시하는 방법이다.
>>>> ##### 1)ERD 작업 순서
>>>> ##### 1.엔터티를 그린다 => 2.엔터티를 적절하게 배치한다. => 3.엔터티 간 관계를 설정한다. => 4.관계명을 기술한다. => 5.관계의 참여도를 기술한다. => 6.관계의 필수여부를 기술한다.
>>>> 
