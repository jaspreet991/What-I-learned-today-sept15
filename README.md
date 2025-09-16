# What-I-learned-today-sept15
Ceiling of a number: 
Ques type: Binary search
Description: ceiling of a number is the smallest element greater than or equal to the target element.
Similar: floor of an element
code-
public class ceiling {
    public static void main(String[] args) {
        int[] num = {2,3,5,9,14,16,18};
    int target =15;
    int ans = go(num,target);

    }
    static int go(int [] num, int target){
        int start = 0;
        int end = num.length-1;
        for(int i=0;i<num.length;i++){
            int mid = start + (end-start)/2;
            if(target==mid){
                return mid;
            }
            if(target>mid){
                start = mid+1;
            }
            if(target<mid){
                end = mid-1;
            }
        }
return num[start];



    }

}


