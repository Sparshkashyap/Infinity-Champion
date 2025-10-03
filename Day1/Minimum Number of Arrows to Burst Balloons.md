Minimum Number of Arrows to Burst Balloons:

class Solution {
    public int findMinArrowShots(int[][] points) {

        Arrays.sort(points,(a,b) -> Integer.compare(a[1],b[1]));
        long temp = Long.MIN_VALUE;
        int c = 0;
        for(int arr[]:points){
           
            if(arr[0]>temp){
                c++;
                temp = arr[1];
            }
        }

        return c;
        
    }
}




