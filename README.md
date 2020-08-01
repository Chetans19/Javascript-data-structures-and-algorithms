# Javascript-data-structures-and-algorithms

 All data structures and algorithms implemented in javascript will be uploaded here.

 - [Searching Algorithms](#searching-algoorithms)
    * [Linear search](#linear-search)
    * [Binary search](#binary-search) 
    
 - [Soring algorithms](#sorting-algorithms)   
 - [Bubble sort](#bubble-sort)
 - [Selection sort](#selection-sort)
 - [Insertion sort](#insertion-sort)
 - [Mergr sort](#merge-sort)
 - [Quick sort](#quick-sort)
 - [Radix sort](#radix-sort)


## Bubble sort
 ``` 
 // UNOPTIMIZED VERSION OF BUBBLE SORT
function bubbleSort(arr){
  for(var i = arr.length; i > 0; i--){
    for(var j = 0; j < i - 1; j++){
      console.log(arr, arr[j], arr[j+1]);
      if(arr[j] > arr[j+1]){
        var temp = arr[j];
        arr[j] = arr[j+1];
        arr[j+1] = temp;         
      }
    }
  }
  return arr;
}

// ES2015 Version
function bubbleSort(arr) {
  const swap = (arr, idx1, idx2) => {
    [arr[idx1], arr[idx2]] = [arr[idx2], arr[idx1]];
  };

  for (let i = arr.length; i > 0; i--) {
    for (let j = 0; j < i - 1; j++) {
      if (arr[j] > arr[j + 1]) {
        swap(arr, j, j + 1);
      }
    }
  }
  return arr;
}

bubbleSort([8,1,2,3,4,5,6,7,8,9,10]);
 ```
## Insertion sort

```
function insertionSort(arr) {
  
  for(var i=0; i<arr.length; i++) {
    let j = i-1;
    let temp = arr[i];
    while(j>=0 && arr[j] > temp) {
      arr[j+1] = arr[j]
      j--;
    }
    arr[j+1] = temp;
  }
return arr;
}

insertionSort([20,3,2,5,89,29,4]);
```
## Merge sort

```
 function merge (left, right) {
  let resultArray = [], leftIndex = 0, rightIndex = 0;

  // We will concatenate values into the resultArray in order
  while (leftIndex < left.length && rightIndex < right.length) {
    if (left[leftIndex] < right[rightIndex]) {
      resultArray.push(left[leftIndex]);
      leftIndex++; // move left array cursor
    } else {
      resultArray.push(right[rightIndex]);
      rightIndex++; // move right array cursor
    }
  }

  // We need to concat here because there will be one element remaining
  // from either left OR the right
  return resultArray
          .concat(left.slice(leftIndex))
          .concat(right.slice(rightIndex));
}
```
 
 
 
 
 
