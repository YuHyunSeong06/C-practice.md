```c
// 1번 문제 : 세 수를 입력받아서 그 중에 최댓값을 반환하는 함수를 만들고 그 함수의 반환값을 출력하라.
#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>

int max(int a, int b, int c) {
	if (a > b && a > c) {
		return a;
	}
	else if (b > c && b > a) {
		return b;
	}
	else
		return c;
}

int main()
{
	int a, b, c;
	scanf("%d %d %d", &a, &b, &c);
	int r = max(a, b, c);
	printf("%d", r);
}
```

```c
// 2번 문제 : 두 수를 키보드로 입력받고 함수를 통해서 출력하시오

#include < stdio.h>

int Add(int a, int b) {
	return a + b;
}

int main() {
	int a, b;
	scanf("%d %d", &a, &b);
	printf("%d", Add(a, b));
}
```

```c
// 3번 문제 : 팩토리얼 함수를 만드시오 힌트: 재귀함수 사용
/*
	1. if 문으로 종료코드를 지정하고
	2. 가장 처음으로 반환되는 숫자는 1이다.*/

#include <stdio.h>

int fac(int n) {
	if (n == 1) {
		return 1;
	}
	return fac(n - 1)*n;
}

int main()
{
	int n;
	scanf("%d", &n);
	printf("%d", fac(n));
}
```

```c
// 4번 문제 : 배열 {4, 3, 1, 2, 5}의 평균 구하기

#include <stdio.h>

int avg(int a[]) {
	int sum = 0;
	for (int i = 0,n=5; i < n;i++) {
		sum += a[i];
	}
	return sum / 5;
}	
int main()
{
	int a[] = { 4,3,1,2,5 };
	printf("%d", avg(a));
}
```

```c
// 5번 문제 : 배열의 크기가 미지수일떄 위 배열의 평균 구하기

#include <stdio.h>

int avg(int arr[],int n) {
	int sum = 0;
	for (int i = 0; i < n;i++) {
		sum += arr[i];
	}
	return sum / (n);
}
int main()
{
	int arr[] = { 4,3,1,2,5,0,79 };
	int a = sizeof(int);
	int b = sizeof(arr);
	
	printf("%d", avg(arr,b/a));
}
```
