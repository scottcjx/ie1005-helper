# ie1005-helper

`With compliments, Scott CJX`

PS. I like kopi peng. I accept googlepay, paynow, [paylah](https://scottcjx.github.io/rsc/plspaylahme.jpg)

- @ [biz@carou](https://www.carousell.sg/p/programming-coding-help-consultation-1196819850/)
- @ [email: scottcjx.w@gmail.com](mailto:scottcjx.w@gmail.com)
- @ [tele: scjxw](https://t.me/scjxw)
- @ [github: scott-cjx](https://github.com/scott-cjx)

This assignment is programmed wholly in C, here are some functions that need to be implemented. 

## required functions

- [`inverse()`](#inverse)
- [`digit_print()`](#digit_print)
- [`random_range()`](#)

## optional functions

 - [`digit_number()`](#digit_number)


### digit_number
gets digit at position n of num

``` c
int digit_number(int num, int n)
{
    int tmp;
    tmp = num / pow(10, n)
    tmp = tmp % 10;
    return tmp;
}
```

### inverse
inverse number

``` c
int inverse(int num)
{
    int len = (int) log10((double)num) + 1;
    int inv_num = 0;
    for (int i = 0; i < len; i++)
    {
        inv_num += digit_number(num, i) * pow(10, len-i);
    }
    return inv_num;
}
```

### digit_print
prints digits with mask "N" at position n

``` c
int digit_print(int num, int n)
{
    int len = (int) log10((double)num) + 1;
    for (int i = 0; i < len; i++)
    {
        if (i == n) 
        {
            printf("N");
        } else 
        {
            printf("%d", digit_number(num, i));
        }
    }
    printf("\n");
}
```

### random_range
get a random number
``` c
// im lazy to do this fr

#include <time.h>
#include <stdlib.h>

int random_range(int max_val)
{
    return time.now() % num_digits;
}
```

## License
This project is available under the GPL v3 license. See the [LICENSE](./LICENSE.md) file for more info.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) 
