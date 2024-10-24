# EX.10 SIMULATION OF DIFFIE HELLMAN ALGORITHM
## AIM:
To implement key exchange between users using Diffie Hellman algorithm.

## ALGORITHM:
•Get the input for prime number p.
•Calculate the primitive root of p that is g.
•Calculate private keys for both users using p and g values.
•Similarly, secret keys for both users are calculated.

## PROGRAM:
```
#include <math.h>
#include <stdio.h>
long long int power(long long int a, long long int b,
long long int P)
{
    if (b == 1)
    return a;
    else
    return (((long long int)pow(a, b)) % P);
}
int main()
{
    long long int P, G, x, a, y, b, ka, kb;
    
    printf("\n                  *****Diffie-Hellman Key Exchange algorithm*****\n\n");
    printf("\n\nEnter the value of P: ");
    scanf("%lld",&P); 
    printf("The value of P: %lld\n", P);
    printf("Enter the value of G (Primitive root of P): ");
    scanf("%lld",&G); 
    printf("The value of G: %lld\n\n", G);
    
    a = 4; 
    printf("The private key a for Alice : %lld\n", a);
    x = power(G, a, P);
    b = 3; 
    printf("The private key b for Bob : %lld\n\n", b);
    y = power(G, b, P); 
    ka = power(y, a, P); 
    kb = power(x, b, P); 
    printf("Secret key for the Alice is : %lld\n", ka);
    printf("Secret Key for the Bob is : %lld\n", kb);
    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/2f2f539f-9742-4029-8a15-4577f9022d2b)
## RESULT:
Hence, the simulation of Diffie Hellman algorithm is successfully done.
