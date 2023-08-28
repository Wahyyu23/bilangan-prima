// bilangan-prima
// Program yang menampilkan bilangan prima diatara dua bilangan

#include <stdio.h>
#include <math.h>

int main()
{
    int start, end;

    printf("Masukkan nilai awal dan akhir\n");
    scanf("%d%d", &start, &end);

    if (start > end)
    {
        int temp = start;
        start = end;
        end = temp;
    }

    printf("Bilangan Prima antara %d dan %d adalah:\n", start, end);

    for (int num = start; num <= end; num++)
    {
        int prime = 1;
        int inum = sqrt(num);
        for (int count = 2; count <= inum; count++)
        {
            if (num % count == 0)
            {
                prime = 0;
                break;
            }
        }

        if (prime)
            printf("%d,\t", num);
    }

    return 0;
}


