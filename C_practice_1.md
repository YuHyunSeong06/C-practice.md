```c
// 1번 문제 마일 값을 미터 값으로 변환하기

#define _CRT_SECURE_NO_WARNINGS 
#include <stdio.h>
#define METER 1.609


int main()
{
	float mile,r;
	scanf("%f", &mile);
	r = METER * mile;
	printf("%f meter",r );
}
```

```c
// 2번 문제 일당 3만원일때 날짜 입력받고 금액 구하기

#define _CRT_SECURE_NO_WARNINGS 
#include < stdio.h>
#define CASH 3

int main()
{
	int day, r;
	scanf("%d", &day);
	r = CASH * day;
	printf("%d만원", r);
}
```

```c
// 3번 문제 키보드로부터 두 수를 입력받아 삼각형의 넓이 구하기
#define _CRT_SECURE_NO_WARNINGS 
#include <stdio.h>

int main()
{
	int w, h;
	float r;
	scanf("%d %d", &w, &h);
	r = (float)(w * h) / 2;
	printf("%f", r);

}
```

```c
// 4번문제 두 수를 입력받아 크기가 큰 값이 출력되게하기

#include <stdio.h>

int main()
{
	float a, b;
	scanf("%f%f", &a, &b);
	if (a - b>0) {
		printf("%f", a);
	}
	else { 
		printf("%f", b); 
	}
}
```

```c
// 5번문제 세 수를 입력받아 가장 큰 값을 출력하기
/*
	1. 세 수를 입력받는다
	2. a, b를 비교
	3. 더 큰 수와 c를 비교
	4. 가장 큰 수를 출력
	간소화
		v
	1. 세 수를 입력받는다
	2. a, b를 비교 && a, c를 비교
	3. b, a를 비교 && b, c를 비교
	4. 나머지는 c*/

#include <stdio.h>

int main()
{
	int a, b, c;
	scanf("%d%d%d", &a, &b, &c);
	if (a > b && a > c) {
		printf("%d", a);
	}
	else if (b > a && b > c) {
		printf("%d", b);
	}
	else {
		printf("%d", c);
	}
}
```

```c
// 6번 문제 5월 1일은 월요일이다. 날짜를 입력받아 몇요일인지를 구하여라
/*
	1. 날짜를 입력받는다. 이때 날짜는 31을 초과할 수 없다.
	2. 일주일이 7일 인것을 이용한다
	3. 입력받은 수를 7로 나눠 나머지에 따라 요일을 정한다. */
#include <stdio.h>

int main()
{
	int day;
	scanf("%d", &day);
	if (day > 31||day<=0) {
		printf("올바른 날짜를 입력해주십시오.");
	}
	else {
		switch (day % 7)
		{
		case 1: printf("월요일입니다.");
			break;
		case 2: printf("화요일");
			break;
		case 3: printf("수요일");
			break;
		case 4: printf("목요일");
			break;
		case 5: printf("금요일");
			break;
		case 6: printf("토요일");
			break;
		default:printf("내일은 월요일");
			break;
		}
	}
}
```

```c
// 7번 문제 * 표시를 5줄로 10개씩 출력하기
/*
	1. 5줄을 먼저 for 문을 통해서 센다
	2. 다중 for 문을 이용해 *을 10개 찍는다
	3. *을 출력한다.*/
#include <stdio.h>

int main()
{
	int p, q;
	for (p = 0; p < 5; p++) {
		for (q = 0; q < 10; q++) {
			printf("*");
		}printf("\n\n");
	}
}
```

```c
// 8번 문제 구구단을 2단부터 9단까지 출력하기
/*
	1. for 문을 이용해 9단까지 만든다
	2. 다중 for 문을 통해 1부터 9까지 곱한다.
	3. 구구단을 출력한다. */

#include <stdio.h>

int main()
{
	int p, q;
	for (p = 2; p < 10; p++) {
		printf("%d단\n\n", p);
		for (q = 1; q < 10; q++) {
			printf("%d*%d=%d\n",p, q, p * q);
		}printf("\n\n");
	}
}
```

```c
// 9번 문제 정수를 끊임없이 입력받고 -1이 종료코드가 되게하시오.
/*. 
	1. while 문을 통해 무한반복되게 만든다.
	2. 정수들을 입력받는다
	3. -1를 종료코드로 설정한다.
	4. 모두 더한값을 출력한다.*/

#include <stdio.h>

int main()
{
	int p = 0;
	int sum = 0;
	while (p!=-1) {
		sum += p;
		scanf("%d", &p);
	}
	printf("%d", sum);
}
```

```c
// 10번 문제 0부터 100까지 3의 배수를 모두 더하다가 100 이상이 되면 멈춰라
/*
	1. p와 sum이라는 변수를 선언한다.
	2. p와 sum 값을 각각 0으로 초기화한다.
	3. for 문이나 while 문을 통해 p의 값을 반복한다
	4. 반복된 값중 3의 배수일 경우에 sum에 p를 더한다.
	5. 3의 배수가 아닐경우 폐기한다.
	6. 만약 sum 값이 100이 넘어갈 경우에 멈춘다.
	*/

#include <stdio.h>

int main() {
	int p , sum=0;
	for (p = 0; p < 101; p++) {
		if (p % 3 == 0) {
			sum += p;
			if (sum >= 100) {
				printf("%d", sum);
				break;
			}
		}
	}
}
```

```c
// 11번 문제 continue 문을 사용에서 1 부터 10까지 수 중에 4를 뺴고 출력하라.

#include <stdio.h>

int main()
{
	int p;
	for (p = 1; p < 11; p++) {
		if (p == 4) {
			continue;
		}
		printf("%d ", p);
	}
}
```

```c
// 12번 문제 정수 배열을 10,20,30,40,50으로 초기화하고 배열의 내용을 50부터 역순으로 출력
/*
	1. 크기 5인 배열을 선언한다.
	2. 배열을 역순으로 출력*/
#include <stdio.h>

int main()
{
	int arr[5]={ 10,20,30,40,50 };
	int p=4;
	for (; p >= 0; p--) {
		printf("%d ", arr[p]);
	}
}
```

```c
// 13번 문제 정수 배열을 10, 20, 30, 40, 50으로 초기화하고 배열을 모두 더하여라
// 
#include <stdio.h>

int main()
{
	int arr[5] = { 10,20,30,40,50 };
	int p = 0;
	int sum = 0;
	for (;p < 5;p++) {
		sum += arr[p];		
	}printf("%d\n", sum);
}
```

```c
/* 14번 문제 1,3,6 \n 2,4,7\n 5,1,2 중 최댓값 구하기
	1. */

#include <stdio.h>

int main()
{
	int arr[3][3] = { {1,3,6},{2,4,7},{5,1,2} };
	int sum = 0;
	for (int p = 0; p < 3; p++) {
		for (int q = 0;q < 3;q++) {
			printf("%d\t", arr[p][q]);
			sum += arr[p][q];
		}
		printf("\n\n");
	}
	int max = arr[0][0];
	for (int p = 0; p < 3; p++) {
		for (int q = 0;q < 3;q++) {
			if (max <= arr[p][q]) {
				max = arr[p][q];
			}
		}
		
		
	}
	printf("%d\n", sum);
	printf("%d\n", max);
}
```
