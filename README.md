# Experiment-20
c plus plus and data structures experiment 20

AIM:- To learn and implement sorting algorithms

Software used:- VS code

Theory:-
Sorting algorithms arrange data in a particular order (ascending or descending) to make searching and processing more efficient. Common sorting algorithms include

1).Bubble Sort: Repeatedly swaps adjacent elements if they are in the wrong order. It's simple but inefficient for large datasets (O(n²) time complexity).
2).Selection Sort: Selects the smallest (or largest) element from the unsorted part and swaps it with the first unsorted element. Like Bubble Sort, it’s O(n²) in time complexity.
3).Insertion Sort: Builds a sorted array one element at a time, inserting elements into their correct position. It’s efficient for small or partially sorted arrays with O(n²) complexity.

CODE :-

1).selction sort
```
//Ashu Yadav
//23070123154

#include <iostream>
using namespace std;

void swap(int *a, int *b) 
{
  int temp = *a;
  *a = *b;
  *b = temp;
}


void display(int ar[], int len) 
{
  for (int i = 0; i < len; i++) 
  {
    cout << ar[i] << " ";
  }
  cout << endl;
}

void selectsort(int ar[], int len) 
{
  for (int j = 0; j < len - 1; j++) 
  {
    int mi = j;
    for (int i = j + 1; i < len; i++) 
    {
      if (ar[i] < ar[mi])
        mi = i;
    }

    swap(&ar[mi], &ar[j]);
  }
}

int main() 
{
  int data[] = {50, 25, 10, 15, 30};
  int len = sizeof(data) / sizeof(data[0]);
  cout << "Original Array:";
  display(data, len);
  selectsort(data, len);
  cout << "Selection sorted array:";
  display(data, len);
}
```

2).insertion sort
```
//Ashu Yadav
//23070123154

#include <iostream>
using namespace std;

void insertsort(int ar[], int n) 
{
    for (int i = 1; i < n; i++) 
    {
        int key = ar[i];
        int j = i - 1;

        while (j >= 0 && ar[j] > key) 
        {
            ar[j + 1] = ar[j];
            j = j - 1;
        }
        ar[j + 1] = key;
    }
}

void display(int ar[], int n) 
{
    for (int i = 0; i < n; i++) 
    {
        cout << ar[i] << " ";
    }
    cout << endl;
}

int main() {
    int ar[] = {12, 16, 2, 8, 6};
    int n = sizeof(ar) / sizeof(ar[0]);

    cout << "Original array: ";
    display(ar, n);
    insertsort(ar, n);
    cout << "Insertion Sorted array: ";
    display(ar, n);

    return 0;
}
```
3).bubble sort

```
#include <iostream>
#include <algorithm>
using namespace std;

int main() {
int arr[5] = {10, 17, 27, 4, 6};
int n = 5;

for (int i = 0; i < n; i++) {
    for (int j = 0; j < n - 1; j++) { 
        if (arr[j] > arr[j + 1]) { 
            swap(arr[j], arr[j + 1]); 
        }
    }
}

cout << "The sorted array will be: ";
for (int i = 0; i < n; i++) {
    cout << arr[i] << " ";
}
cout << endl;

return 0;
}
```



Conclusion:-in this experiment we learnt about the sorting algorithms.
