# **CHAPTER 2. SQL 기본 및 활용**

### 27. SELECT문의 구성
**FROM**

**WHERE**

**GROUP BY**
- 특정 칼럼을 기준으로 그룹화하여 각 그룹에 대해 집계 연산을 수행할 때 사용하는 절 
- COUNT, SUM, AVG, MAX, MIN 등 집계함수랑 쓰임
- SELECT절에는 집계함수와 개별 칼럼을 함께 사용할 수 있으나, *개별 칼럼은 반드시 GROUP BY 절에 명시된 그룹화 기준 칼럼*이어야 함 -> *집계되지 않은 칼럼이 GROUP BY 절에 없으면 오류 발생*
- 테이블 전체가 하나의 그룹인 경우 GROUP BY 절을 생략할 수 있음

**HAVING**
- GROUP BY 절과 함께 사용
- 그룹화된 데이터에 조건 적용 시 사용
- *WHERE 절은 GROUP BY 절보다 먼저 실행*되므로 집계 함수 조건을 지정할 수 없기에 
*집계 결과 조건은 반드시 HAVING 절에서 처리*

**SELECT**

**ORDER BY**
- ASC
- DESC

**ALL**

**DISTINCT**


### 28. 문자형 함수
**LOWER( )**

**UPPER( )**

**ASCII( )**

**CHR( )**

**SUBSTR(문자열, m, [, n])**

**INSTR(문자열, 찾을문자열 [,m[, n]])** *검색 시작 위치/몇번째로 나타나는 문자열을 찾을지*

**LTRIM(문자열, 삭제문자열)**

**RTRIM(문자열, 삭제문자열)**

**TRIM(문자열)**

**CONCAT(문자열1, 문자열2)** *문자열 두 개 이어붙이기*

**LENGTH(문자열)**

**REPLACE(문자열, 바꿀문자열, 대체문자열)**



### 29. 숫자형 함수
**ABS(숫자)**

**SIGN(숫자)**

**MOD(숫자1, 숫자2)**

**CEIL(숫자)**

**FLOOR(숫자)**

**ROUND(숫자 [, m])**

**TRUNC(숫자 [, m])**



### 30. 변환형 함수
**TO_CHAR(숫자/날짜, FORMAT)**

**TO_NUMBER(문자열)**

**TO_DATE(문자열, FORMAT)**

**CAST(표현식 AS 데이터형)**


### 31. 날짜형 함수
**SYSDATE**

**EXTRACT('YEAR'|'MONTH'|'DAY' FROM 날짜)**

**TRUNC(날짜 [, 단위])**

**ADD_MONTHS(날짜, n)**



### 32. 기타 함수
**CASE 표현식**

**DECODE(표현식, 기준값1, 출력값1 [, 기준값2, 출력값2, ... , 디폴트값])**

**NVL(표현식, 대체값)**

**NVL2(표현식, 대체값1, 대체값2)**

**NULLIF(표현식1, 표현식2)**

**COALESCE(표현식1, 표현식2, 표현식3 ...)**