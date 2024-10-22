# CDS.EXP-20
# EXP-20


#### Aim 
To study and implement sorting algorithm C++. 

#### Software 
Visual Studio Code 

#### Theory 
<ul>
    Sorting algorithms are used to rearrange elements of a list in a specific order, typically either ascending or descending. Below, I'll explain a few common sorting algorithms in C++.

1. Bubble Sort
Bubble Sort repeatedly compares adjacent elements and swaps them if they are in the wrong order. This process is repeated until the list is sorted.

2. Selection Sort
Selection Sort finds the minimum element from the unsorted part of the list and swaps it with the first unsorted element. It repeats this process until the list is sorted.

3. Insertion Sort
Insertion Sort builds the sorted list one item at a time by repeatedly taking one unsorted item and inserting it into the correct position within the sorted part of the list.

</li>
</ul>

#### Code 

(A) <br> 
```cpp
//AKALP SARKAR
//23070123116
//EXP 20 A
//ENTCB2
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;
    int arr[no_el];

    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    s_sort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}
```

#### Output 
![OUTPUT20A](https://github.com/user-attachments/assets/3d90b88a-af2e-4519-942a-31b00eb6c2b3)


(B) <br> 
```cpp
//AKALP SARKAR
//23070123116
//EXP 20 B
//ENTC B2
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;

    int arr[no_el];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    bubbleSort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
} 
```

#### Output 
![OUTPUT20B](https://github.com/user-attachments/assets/1483222e-66f4-45b4-b8b3-974e65490acd)

(B) <br> 
```cpp
//AKALP SARKAR
//23070123116
//EXP 20 C
//ENTC B2
#include<iostream>
using namespace std;

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead of their current position
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int n;
    cout << "How many elements in your array?" << endl;
    cin >> n;
    
    int arr[n];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    insertionSort(arr, n);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
}
```

#### Output 
![OUTPUT20C](https://github.com/user-attachments/assets/f7326824-8215-49ea-811c-01b024f8d4be)

#### Conclusion 
I learnt the study and implement sorting algorithm C++.
