# merge-sort
#include<iostream>
using namespace std;
void merge(int array[],int start,int mid,int close){
    
    
}
void mergesort(int array[],int begin,int end){

    if(begin>end)
    return;
    
    int mid;
    mid=begin+(end-begin)/2;
    
    mergesort(array,begin,mid);
    mergesort(array,mid+1,end);//recursive call
    
    merge(array,begin,mid,end);
}
void print(int array[],int size){
    int i;
    for(i=0;i<size;i++){
        cout << array[i] << endl;
    }
}
int main(){
    int i,n,size;
    cout << "Enter Array size" << endl;
    cin >> n;
    int array[n];
    cout << "Enter your Array" << endl;
    for(i=0;i<size;i++){
        cin >> array[i];
    }
    size = sizeof(array)/sizeof(array[0]);
    mergesort(array,0,size-1);
    print(array,size);
    return 0;
}
