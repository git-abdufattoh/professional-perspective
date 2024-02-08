# professional-perspective
#include <stdio.h>
#include<stdlib.h>
#include<time.h>


int main() 
{
srand(time(NULL)); /*by including this we are ensuring that numbers won't be repeated*/
int array [50];
int i;
while(i<50)//generating numbers until the limited set
{
    int random=(rand() % 999)+1;
    int duplicate=0;
     // to check whether number is repeated
    for(int i = 0; i<50 ; i++)
    {
        if (array[i] == random)
        {
            duplicate=1;
            break;
        }
    }
     if (!duplicate) {
            array[i] = random;
  printf("%03d ", array[i]); /* Display the number in 3-digit format*/
  //Print a newline after every 5 numbers for readability
              if ((i + 1) % 5 == 0) {
                printf("\n");
}
i++;
}
}
}
