# Interview-Prep
#React 19  features
- its introduces new complier 
- it has made useMemo and useCallback hook obselute thanks to react 19 complier
-  added build in support for metadata
-  build in support for  use client and use server directive
-  
![Screenshot (4)](https://github.com/user-attachments/assets/83019986-dac0-44dd-892f-d56c7685a71f)
![Screenshot (7)](https://github.com/user-attachments/assets/0fcda7db-3357-4e29-ab46-4337ae9fe3e8)
#React 19 course
https://www.youtube.com/watch?v=M9O5AjEFzKw&t=156160s
https://www.youtube.com/watch?v=znZQFzoV3CM&list=PLSDeUiTMfxW5vCie_cwsV6UPcZijHce8j&index=15

program to remove duplicate from array 
const nums1 = [1,1, 2, 3, 0, 0, 0];

const uniqueArray = nums1.filter((value, index, array) => array.indexOf(value) === index);

console.log(uniqueArray); // Output: [1, 2, 3, 0]

merge sorted array program 
function merge(nums1, m, nums2, n) {
    let i = m - 1; // Pointer for nums1
    let j = n - 1; // Pointer for nums2
    let k = m + n - 1; // Pointer for the end of nums1
    while (i >= 0 && j >= 0) {
        if (nums1[i] > nums2[j]) {
            nums1[k] = nums1[i];
            i--;
        } else {
            nums1[k] = nums2[j];
            j--;
        }
        k--;
    }
    while (j >= 0) {
        nums1[k] = nums2[j];
        j--;
        k--;
    }
    return nums1;
}

// Example usage
const nums1 = [1, 2, 3, 0, 0, 0];
const m = 3;
const nums2 = [2, 5, 6];
const n = 3;

const result = merge(nums1, m, nums2, n);
console.log(result); // Output: [1, 2, 2, 3, 5, 6]


remove all occurence of element from array
function removeElement(num,val){
let k = 0;
// 1 3 4 5 6 2
//[1,2,3,4,5,6,2]; k=5
for(let i=0;i<=num.length-1;i++){
    if(num[i]!==val){
    num[k]=num[i];
    k++;
    }
}
return k;
}

let num = [1,2,3,4,5,6,2]

console.log(removeElement(num,2));
let k1= removeElement(num,2);
console.log(num.slice(0,5));
