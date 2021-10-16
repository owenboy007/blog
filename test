```java
public class Solution {
  public int[] kSmallest(int[] array, int k) {
    // Write your solution here
    int[] res = new int[k];
    int left = 0, right = array.length - 1;
    res = quickSelect(array, left, right, k);
    Arrays.sort(res);
    return res;
  }

  private int[] quickSelect(int[] arr, int left, int right, int k) {
    while(left <= right) {
      int pivot = partition(arr, left, right);
      if (pivot == k - 1) {
        return Arrays.copyOfRange(arr, 0, k);
      } else if (pivot > k - 1) {
        right = pivot - 1;
      } else {
        left = pivot + 1;
      }
    }
    return new int[k];
  }

  private int partition(int[] arr, int left, int right) {
    int pivot = left + rand.nextInt(right - left + 1);
    swap(arr, pivot, right);
    int i = left, j = right - 1;
    while (i <= j) {
      if (arr[i] < arr[right]) {
        i++;
      } else {
        swap(arr, i, j--);
      }
    }
    swap(arr, i, right);
    return i;
  }

  private void swap(int[] arr, int a, int b) {
    int tmp = arr[a];
    arr[a] = arr[b];
    arr[b] = tmp;
  }

  private Random rand = new Random();
}
```
