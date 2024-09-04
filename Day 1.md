# Day 1

## Data Structures and Algorithms

-   Revised concept of Backtracking
-   Permutations using backtracking
-   N queens(solved)

### Problem Solved : 1652 (Defuse the Bomb)

```java
class Solution {
    public int[] decrypt(int[] code, int k) {
        int []arr=new int [code.length];
        if(k>0){
            for(int i=0;i<code.length;i++){
                for(int j=1;j<=k;j++){
                    arr[i]+=code[(i+j)%code.length];
                }
            }
        }else if(k==0){
            for(int i=0;i<code.length;i++){
                arr[i]=0;
            }
        }else{
            for(int i=0;i<code.length;i++){
                for(int j=-1;j>=k;j--){
                    arr[i]+=code[(i+j+code.length)%code.length];
                }
            }
        }
        return arr;
    }
}
```

## WEB - DEVELOPMENT

-   Diffrence between synchronous and Asnchronous languages
-   How javascript is synchronous language
-   Async functions in javascript
-   Await keyword
-   What are promises
