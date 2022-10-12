# :computer: Try Baekjoon

## 조건문
+ 2753번
  + 연도가 주어졌을 때, 윤년이면 1, 아니면 0을 출력하는 프로그램을 작성하시오. 윤년은 연도가 4의 배수이면서, 100의 배수가 아닐 때 또는 400의 배수일 때이다
  
  ```c
  int main(void) {

	int A;

	scanf("%d", &A);

	if (A % 4 == 0 && A % 100 != 0 || A % 400 == 0) {
		printf("1");
	}
	else {
		printf("0");
	}
	
	return 0;}
  ```
  
+ 14681번
	+ 점의 좌표를 입력받아 그 점이 어느 사분면에 속하는지 알아내는 프로그램을 작성하시오.
	
```c
int main(){
    int x, y;
    scanf("%d %d". &x, &y);
    
    (x>0) ? ((y>0) ? (printf("1")):(printf("2"))):((y>0) ? (printf("4")):(printf("3")));}
```

  
+ 2884번
  + 원래 설정되어 있는 알람을 45분 앞서는 시간으로 바꾸는 것이다. 현재 상근이가 설정한 알람 시각이 주어졌을 때, 창영이의 방법을 사용한다면, 이를 언제로 고쳐야 하는지 구하는 프로그램을 작성
  ```c
  int main(void) {

	int H, M;

	scanf("%d %d", &H, &M);

	if (M - 45 < 0) {
		H -= 1;
		M = 15 + M;
		if (H < 0) {
			H += 24;
		}
	}
	else {
		M -= 45;
	}
	printf("%d %d", H, M);

	return 0;}
  ```

## 반복문
## 1차원 배열
+ 10818번
  + N개의 정수가 주어진다. 이때, 최솟값과 최댓값을 구하는 프로그램을 작성하시오.
  
  ```c
  
  int main(void){
    int n;
    int arr[1000000];
    int max, min;
    
    scanf("%d", &n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    max = arr[0];
    min = arr[0];

    for (int i = 0; i < n; i++) {
        if (max < arr[i]) {
            max = arr[i];
        }
        else if (min > arr[i]) {
            min = arr[i];
        }
    }
    printf("%d %d", min, max);

    return 0;}
  ```
<br/>

+ 2562번
  + 9개의 서로 다른 자연수가 주어질 때, 이들 중 최댓값을 찾고 그 최댓값이 몇 번째 수인지를 구하는 프로그램을 작성하시오.
<br>
  
```c
  int main(){
    int arr[9];
    int max = 0, n;

    for (int i = 0; i < 9; i++) {
        scanf("%d", &arr[i]);
        if (max < arr[i]) {
            max = arr[i];
            n = i;
        }
    }
    printf("%d\n%d", max, n + 1);
    
    return 0;}
```
    
<br>

+ **3052번**
  + 두 자연수 A와 B가 있을 때, A%B는 A를 B로 나눈 나머지 이다. 예를 들어, 7, 14, 27, 38을 3으로 나눈 나머지는 1, 2, 0, 2이다. 
수 10개를 입력받은 뒤, 이를 42로 나눈 나머지를 구한다. 그 다음 서로 다른 값이 몇 개 있는지 출력하는 프로그램을 작성하시오.
<br>

```c
 int main(){
    int arr[10], n[10], count, num = 0;
    

    for (int i = 0; i < 10; i++) {
        scanf("%d", &arr[i]);
        n[i] = arr[i] % 42;
    }
    for (int i = 0; i < 10; i++) {
        count = 0;
        for (int j = 0; j < i; j++) {
            if (n[i] == n[j]) {
                count++;
            }
        }
        if (count == 0) {
            num++;
        }
    }
    printf("%d", num);
    
    return 0;}
```
