#include <ctype.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main(void)
{
    char s[50];
    printf("S: ");
    scanf("%s", s);

    char *t;
    t = malloc(strlen(s) + 1);

    if (t == NULL)
    {
        return 1;
    }

    strcpy(t, s);

    if (strlen(t) > 0)
    {
        t[0] = toupper(t[0]);
    }

    printf("S: %s\n", s);
    printf("T: %s\n", t);

    free(t);
    
    }
