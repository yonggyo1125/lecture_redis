## Redis 자료형

- 데이터 타입에 따라 명령어가 다르다.
- 대소문자 구별을 하지 않기 때문에 명령어를 대문자/소문자 구분없이 작성 가능

### Strings

- 문자열, 숫자 serialized object(JSON)등 여러 자료형을 저장하는 Strings Type이다.
- 레디스는 자료형에 상관없이 모두 strings로 저장한다.
- strings로 저장되어도 사칙 연산이 가능하다.

#### strings 명령어

- `SET`, `GET` : `key-value`쌍인 구성으로, SET으로 값을 설정하고 GET으로 값을 조회한다.

```
SET team1 lee
GET team1
"lee"
```

- `MSET`, `MGET` : 여러값을 지정(SET)하고, 조회(GET) 할수 있음

- 숫자 형태 Strings 저장할 때
  - `INCR`: 숫자형 string 값을 1씩 증가
  - `INCRBY`: 숫자형 string값을 지정한 만큼 증가

```
SET price 10
INCR price  # price: 11
INCRBY price 9 # price: 20
```
