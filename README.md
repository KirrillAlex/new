#include<iostream>
#include<cmath>

using namespace std;

int Max(int *a, int n){
    int M = 0, z;
    for(int i = 0; i < n; i++){
            if (a[i] < M) M = a[i];
            z = i;
    }
    return z;
}

int check(int *a, int n, int M){
    bool f = true;
    for(int i = 0; i < n; i++){
        if (a[i] > a[M]) f = false;
    }
        if (f == true){
            cout << "Function is working";
        }
        else {
            cout << "Function is not working";
        }
}

int main(){
    int a[] = {1, 3, 5, 8, 10};
    int z;
    z = Max(a, 5);
    cout << "Index = " << z << endl;
    check(a, 5, z);
}
