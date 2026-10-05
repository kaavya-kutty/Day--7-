# Day--7-
#include <stdio.h>

void swap(int *a, int *b)
{
    int temp;

   temp = *a;
    *a = *b;
    *b = temp;
}

int main()
{
    int num1, num2;

  printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

   printf("Before swapping: num1 = %d, num2 = %d\n", num1, num2);

  swap(&num1, &num2);
    printf("After swapping: num1 = %d, num2 = %d\n", num1, num2);

  return 0;
}
#include <stdio.h>

int main()
{
    int arr[100], n, i, temp;
    int *start, *end;

  printf("Enter the size of the array: ");
    scanf("%d", &n);

   printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }

   start = arr;
    end = arr + n - 1;

  while (start < end)
    {
        temp = *start;
        *start = *end;
        *end = temp;

  start++;
        end--;
    }

  printf("Reversed array: ");
    for (i = 0; i < n; i++)
    {
        printf("%d ", arr[i]);
    }

   return 0;
}
#include <stdio.h>

int main()
{
    int arr[100], n, i;
    int *ptr;
    int max, min;

  printf("Enter the size of the array: ");
    scanf("%d", &n);

   printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }

  ptr = arr;

  max = *ptr;
    min = *ptr;

   for (i = 1; i < n; i++)
    {
        ptr++;

  if (*ptr > max)
        {
            max = *ptr;
        }
 if (*ptr < min)
        {
            min = *ptr;
        }
    }
    printf("Maximum element = %d\n", max);
    printf("Minimum element = %d\n", min);

  return 0;
}
