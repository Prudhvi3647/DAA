#include<iostream>  
using namespace std;  
int main ()  
{    
    int myarray[100] = { 12,4,3,1,11,41,31,21,10,2};   
       
    cout<<"\nInput:\n";
    for(int i=0;i<10;i++)  
    {  
        cout <<myarray[i]<<"\t";  
    }    
    for(int n=1; n<10; n++)   
    {  
        int temp = myarray[n];  
        int j= n-1;  
        while(j>=0 && temp <= myarray[j])  
        {  
            myarray[j+1] = myarray[j];   
            j = j-1;  
        }  
        myarray[j+1] = temp;  
    }  
    cout<<"\nSorted:\n";
    for(int i=0;i<10;i++)  
    {  
        cout <<myarray[i]<<"\t";  
    }  
}
