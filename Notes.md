## R 벡터 실습 정리

### 📌 벡터 생성 및 출력

```r
v1 <- c(1,2,3,4)
v1
# 출력: 1 2 3 4
```

```r
v2 <- -5:5
v2
# 출력: -5 -4 -3 -2 -1 0 1 2 3 4 5
```

```r
v3 <- seq(from=0, to=5, by=0.5)
v3
# 출력: 0.0 0.5 1.0 1.5 ... 5.0
```

```r
v4 <- rnorm(20)
v4
# 출력: 평균 0, 표준편차 1인 정규분포 기반 20개 난수
```

### 📈 기본 통계 및 정렬

```r
mean(v1)                # 출력: 2.5
order(v2)               # 출력: v2를 오름차순 정렬하는 인덱스
rev(v3)                 # 출력: v3를 뒤집은 벡터
range(v1)               # 출력: c(1, 4)
sd(v2)                  # 출력: 표준편차
sort(v4)                # 출력: 오름차순 정렬
sort(v4, decreasing=TRUE)  # 출력: 내림차순 정렬
length(v4)              # 출력: 20
```

### 🔧 벡터 조작

```r
x <- c(1,4,6,8,9)
x[2]                    # 출력: 4
x[-2]                   # 출력: 1 6 8 9
x[2 < x & x < 5]        # 출력: 4
replace(x, c(2,4), c(32,24))  # 출력: 1 32 6 24 9
append(x, y)            # x와 y를 이어붙이기
append(x, y, after=2)   # x의 2번째 이후에 y 삽입
```

### ➕ 벡터 연산

```r
c(1,2) + c(4,5)         # 출력: 5 7
c(1,2,3) + 1            # 출력: 2 3 4
```

### 🔢 집합 연산

```r
x <- c(1,2,3)
y <- c(3,5,6)

x == y                  # 출력: 각 원소 비교 결과
union(x, y)             # 출력: 중복 제거 합집합
intersect(x, y)         # 출력: 교집합 (3)
setdiff(x, y)           # 출력: x - y
setequal(x, y)          # 출력: FALSE
is.element(3, x)        # 출력: TRUE
```

### 🔁 반복과 고유값

```r
x <- rep(c("a","b","c"), times=4)
unique(x)               # 출력: a b c
match(x, c("a"))        # 출력: 1 NA NA 1 NA NA ...
```

### 📎 문자열 결합

```r
y <- c("d", "e", "f")
paste(x[1], y[3])       # 출력: "a f"
```

### ✅ 논리 연산 및 확인

```r
x <- runif(5)
(0.4 <= x) & (x <= 0.7) # 출력: TRUE/FALSE
any(x > 0.8)            # 출력: TRUE 또는 FALSE
all(x < 0.7)            # 출력: TRUE 또는 FALSE
is.vector(x)            # 출력: TRUE
```
