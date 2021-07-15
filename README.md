# New-Public-key-infrastructure
Title: Public Key Infrastructure 
CESAER CIPHER

E(x) = (x+n) mod 26 
D(x) = (x-n) mod 26

#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<stdbool.h>
#include <ctype.h> 


int main (int argc, char *agrv[]
{
  if (argc == 2)
  {
    int key = atoi(argv[1]);
    bool valid_key = False;
    
    for (int i = 0; i < strlen(argv[1]); i++)
    {
    if (isdigit(argv[1][i])
      {
      valid key = true;
      }
      else
       {
    printf("Usage ./cesaer key|n")
    return 1;
  }
    }
    printf("Usage ./cesaer key|n")
    return 1;
  }

  if (valid key == true)
    {
      char input [400]
      printf("plaintext: ");
      fgets(input, sizeof(input), stdin);
      
        for (int i = 0; i < strlen(input); i++)
        {
          if (isupper(input[i]))
          {
              input[i] = input[i] - 65 + key)% 26) + 65;
          }
          else  if (islower(input[i]))
          {
              input[i] = input[i] - 97 + key)% 26) + 97;
          }
        }
        printf("Cipher: %S", input);
    }
    else
    {
       printf("Usage ./caesar key\n");
        return 1;
    }
}
