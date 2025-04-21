# Sorting-in-C

#include <stdio.h>

void insertionsort(int arr[]) {
    for(int i = 1; i < 5; ++i) {
        int key = arr[i];
        int j = i - 1;

        while(j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--; // Fix: decrement j instead of resetting it
        }
        arr[j + 1] = key;
    }
}

int main() {
    int b[5] = {5,4,3,2,1};
 
    insertionsort(b);

    
    for(int i = 0; i < 5; i++) {
        printf("%d ", b[i]);
    }

    return 0;
}
