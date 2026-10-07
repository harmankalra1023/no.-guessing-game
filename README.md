# no.-guessing-game

#include <stdio.h>
#include <stdlib.h> // Required for rand() and srand()
#include <time.h>   // Required for time()

int main() {
    // 1. Seed the random number generator with the current time
    srand(time(NULL));

    // 2. Generate a random number between 1 and 100
    // rand() % 100 gives a number from 0 to 99. Adding 1 shifts it to 1 to 100.
    int r = (rand() % 100) + 1;


    
    int i=0,n,count=0;//making the body 
    while(i!=r){
        printf("guess the no: \n");
        scanf("%d",&i);
        if(i<r){
            printf("no. is bigger \n");
        }
        if(i>r){
            printf("no. is smaller \n");
        }
        count+=1;
    }
    if(i==r){
        printf("number guessed\n");
    }
    printf("the no. of guesses you took are : %d ",count);//to tell no. of guesses taken
    
    return 0;
}
