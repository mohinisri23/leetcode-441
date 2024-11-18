# leetcode-441
#this file contains the solution of the leetcode question 441: Arranging Coins

int arrangeCoins(int n) {
    int l=0,r=n;
    while(l<=r){
         long mid=(l+r)/2;
        long long int coins=(mid*(mid+1))/2;
        if(coins==n){
            return mid;
        }
        else if(coins<n){
            l=mid+1;
        }
        else{
            r=mid-1;
        }
    }
    return r;
    
}
