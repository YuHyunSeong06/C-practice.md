```c
// for 문으로 1 부터 10 까지 수 중에서 홀수만 출력되게하는 프로그램


#include <stdio.h>

int main()
{
	int a;
	for (int a = 1; a < 11;a++) {
		if (a % 2==1) {
			printf("%d\n", a);
		}
	}
}
```

```c
// while 문으로 위에꺼

#include <stdio.h>

int main()
{
	int a=1;
	while (a < 11) {
		
		if (a % 2 == 1) {
			printf("%d\t", a);
		}
		a++;
	}
}
```

```c
 // 배열 {2, 4, 5, 1, 3} 중 최댓값 구하기

#include <stdio.h>

int main()
{
	int max, a = 0;
	int arr[5] = { 2,4,5,1,3 };
	max = arr[0];

	for(a=1; a<5; a++){
		if (max < arr[a]) {
			max = arr[a];
		}
	}

	printf("%d", max);
}
```

```c
 // 이차원 배열 1, 4, 7\n 2, 5, 8\n 3, 6, 9\n

#include <stdio.h>

int main()
{
	int arr[3][3] = { {1,2,3}, { 4,5,6 }, { 7,8,9 } };
	for (int a = 0; a < 3;a++) {
		for (int b = 0; b < 3;b++) {
			printf("%d ", arr[b][a]);
		}
		printf("\n");
	}
	printf("변수경 수고해라 ㅋ");
}
```

```c
// 이차원 배열 2, 4, 7\n 5, 8, 9,\n 14, 11, 1\n 중 최댓값 구하기

#include <stdio.h>

int main()
{
	int max, a, b;
	int arr[3][3] = { {2,4,7},{5,8,9},{14,11,1} };
	max = arr[0][0];

	for (a = 0;a < 3;a++) {
		for (b = 0;b < 3;b++) {
			if (max < arr[a][b]) {
				max = arr[a][b];
			}
		}
	}printf("%d", max);
}
```
