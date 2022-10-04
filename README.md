# :computer: Try Baekjoon

## 조건문
## 반복문
## 1차원 배열
+ **10818번**
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

+ **2562번**
  + 9개의 서로 다른 자연수가 주어질 때, 이들 중 최댓값을 찾고 그 최댓값이 몇 번째 수인지를 구하는 프로그램을 작성하시오.
  
  
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
