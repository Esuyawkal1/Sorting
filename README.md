#include<iostream>
using namespace std;
void selection_sort(int arr[],int n){
for(int i=0;i<n-1;i++){
int min=i;
for(int j=i+1;j<i;j++){
if(arr[j]<arr[min]){
min=j;
}
}
if(min!=i){
int temp=arr[i];
arr[i]=arr[min];
arr[min]=temp;
}
}
}
void bubble_sort(int arr[],int n){
for(int i=0;i<n;i++){
for(int j=n-1;j>i;j--){
if(arr[j]<arr[j-1]){
int temp =arr[j];
arr[j]=arr[j-1];
arr[j-1]=temp;
}
}
}
}
void insertion_sort(int arr[],int n){
int temp,i,j;
for(i=1;i<n;i++){
 temp=arr[i];
j=i;
while(j>0&&temp<arr[j-1]){
arr[j]=arr[j-1];
j--;
}
arr[j]=temp;
}
}
void display(int arr[],int n){
for(int i=0;i<n;i++){
cout<<arr[i]<<" ";
}
cout<< endl;
}
void displaymenu(int choice){
cout<<"       Sorting \n";
cout << "    ============" << endl;
cout<<"Enter your choice \n";
cout << "1. selection sorting" << endl;
cout << "2. bubble sorting" << endl;
cout << "3. insertion sorting" << endl;
cout << "4. Exit" << endl;
}
int main(){
int choice;
do{
displaymenu(choice);
cout<<"Enter your choice \n";
cin>>choice;
int arr[]={22,54,12,1,3,65,87,11,7};
int n=sizeof(arr)/sizeof(arr[0]);
switch(choice){
case 1:
cout<<"Before sort\n";
display(arr,n);
selection_sort(arr,n);
cout<<"After sort\n";
display(arr,n);
break;
case 2:
cout<<"Before sort \n";
display(arr,n);
bubble_sort(arr,n);
cout<<"After sort\n";
display(arr,n);
break;
case 3:
cout<<"Before sort \n";
display(arr,n);
insertion_sort(arr,n);
cout<<"After sort\n";
display(arr,n);
break;
case 4:
cout<<"exiting program.....\n";
break;
default:
cout<<"invalid choice ! try again. \n";
}


}while(choice!=4);
return 0;
}
