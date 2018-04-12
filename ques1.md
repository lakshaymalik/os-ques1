# os-ques1
Ten students (s1,s2,s3,s4,s5,s6,s7,s8,s9,s10) are going to attend an event. There are lots of gift shops, they all are going to the gift shops and randomly picking the gifts. After picking the gifts they are randomly arriving in the billing counter. The accountant gives the preference to that student who has maximum number of gifts. Create a C program to define order of billed students?
#include <stdio.h>
    void main ()
    {
 
        int num[10];
        int i, j, a, n=10;
   
 
        
        for (i = 0; i < n; ++i){
			printf("Enter the no. of items taken by Student %d \n", i+1);
	        scanf("%d", &num[i]);
 	}
       
 
        for (i = 0; i < n; ++i) 
        {
            for (j = i + 1; j < n; ++j) 
            {
                if (num[i] < num[j]) 
                {
                    a = num[i];
                    num[i] = num[j];
                    num[j] = a;
                }
            }
        }
 
        printf("Order of students:\n");
 
        for (i= 0; i < n; ++i) 
        {
            printf("%d.)Student having %d items\n",i+1,num[i]);
        }
 
    }
