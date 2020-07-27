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

bubbleSort([8,1,2,3,4,5,6,7]);
 ```

 
