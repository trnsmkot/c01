# c01

```c
// ex00
void ft_ft(int *nbr)
{
	*nbr = 42;
}

// ex01
void ft_ultimate_ft(int *********nbr)
{
	*********nbr = 42;
}

// ex02
void ft_swap(int *a, int *b)
{
	int c;

	c = *a;
	*a = *b;
	*b = c;
}

// ex03
void ft_div_mod(int a, int b, int *div, int *mod)
{
	*div = (a / b);
	*mod = (a % b);
}

// ex04
void ft_ultimate_div_mod(int *a, int *b)
{
	int div;
	int mod;

	div = (*a / *b);
	mod = (*a % *b);
	*a = div;
	*b = mod;
}

// ex05
#include <unistd.h>

void ft_putstr(char *str)
{
	while (*str)
	{
		write(1, str, 1);
		str++;
	}
}

// ex06
int ft_strlen(char *str)
{
	int count;

	count = 0;
	while (*str)
	{
		str++;
		count++;
	}
	return (count);
}

// ex07
void ft_rev_int_tab(int *tab, int size)
{
	int new_tab[size];
	int index;

	index = 0;
	while (index < size)
	{
		new_tab[index] = tab[size - index - 1];
		index++;
	}
	*tab = *new_tab;
}

// ex08
void ft_n_swap(int *a, int *b)
{
	int c;

	c = *a;
	*a = *b;
	*b = c;
}

void ft_sort_int_tab(int *tab, int size)
{
	int need_sort;
	int index;

	need_sort = 1;
	while (need_sort > 0)
	{
		index = 0;
		need_sort = 0;
		while (index < size - 1)
		{
			if (tab[index] > tab[index + 1])
			{
				need_sort = 1;
				ft_n_swap(&tab[index], &tab[index + 1]);
			}
			index++;
		}
	}
}
```
