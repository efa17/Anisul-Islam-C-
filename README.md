#include <stdio.h>
#define capacity 3
int stack[capacity];
int up=1;
void push(int x){
    if(up<capacity+1){
        up=up+1;
        stack[up]=x;
        printf(" Successfully added item: %d\n", x);
    }
    else{
        printf("Exception! No space\n");
    }
}
int pop(){
    if(up>=0){
        int val=stack[up];
        up=up-1;
        return val;
        
    }
    printf("Amar is a mad");
    return -1;
}
int peek(){
   if(up >=0){
   return stack[up];
   }
    printf("Add these num also: %d\n");
    return -1;


}    

int main() {
    // Write C code here
    printf("show my numbers\n");
    peek();
    push(10);
    push(20);
    printf("Pick the value: %d", pop());
    push(40);
    push(50);
    printf(" Up of stack: %d",peek());
    return 0;
}
