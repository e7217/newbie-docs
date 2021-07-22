# DATABASE
## DBMS (Database Management System)
+ mssql, postres, mysql, ... etc.

### Primary Key
+ Natural Key
+ Surrogate Key
#### Natural Key
어떤 개체가 갖고 있는 속성을 나타내는 컬럼
#### Surrogate Key
ID 컬럼같은 컬럼, Primary Key를 위해 인위적으로 생성한 컬럼

+ 수정의 용의성으로 Surrogate Key를 더 많이 사용하는 추세
## SQL
### SQL 조건문
```sql
-- 다양한 조건문
 WHERE name BETWEEN A AND B;
 WHERE name NOT BETWEEN A AND B;
 WHERE name IN (A, B);
```
+ 찾아보면 여러가지 조건들이 있음
### SQL 문자열 매칭
```sql 
 WHERE name LIKE 'hello%';
 WHERE name LIKE 'h____%';
```
### 유의사항
+ OR
  - [x] WHERE id = 1 or id =2
  - [ ] WHERE id = 1 or 2 
+ AND와 OR 우선순위
  + AND > OR (default)
  + 더 높이고 싶은 곳에 괄호를 씌워주면 됨
### alias
+ 별칭
```sql
from hello as he from table;
```
### CASE
```sql
CASE 컬럼 이름 
  WHEN 조건 THEN 출력
  WHEN 조건 THEN 출력
  WHEN 조건 THEN 출력
  ELSE 출력
END
```
### 고유값만 보기
+ DISTINCT
```sql
select DISTINCT(gender) from table;
```
### 그루핑
```sql
select gender, count(*) from table group by gender;
```
gender | count(*)
-------|---------
m| 15
f| 13
