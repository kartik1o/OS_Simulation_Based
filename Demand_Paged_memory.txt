#include <stdio.h>
#include <math.h>
#include <conio.h>
int main()
{
double unmodified_pg,modified_page,mat,mod_percentage,eff_access_time,pg_fault_rate;

    printf("                  ****Demand Paged Memory Problem****  \n\n");
    printf("Enter the time for Page Fault not modified in milliseconds: ");
    scanf("%lf", &unmodified_pg);
unmodified_pg =unmodified_pg* pow(10, -3);

    printf("Enter the time for Page Fault modified in milliseconds: ");
    scanf("%lf", &modified_page);
modified_page =modified_page* pow(10, -3); //For taking time in milliseconds

    printf("Enter the time for Memory Access in nanoseconds: ");
    scanf("%lf", &mat);
mat = mat* pow(10, -9);//For taking time in nanoseconds

    printf("Enter  modified percentage: ");
    scanf("%lf", &mod_percentage);
mod_percentage = mod_percentage / 100;

    printf("Enter the time for Efficiency Access in nanoseconds: ");
    scanf("%lf", &eff_access_time);
eff_access_time =eff_access_time* pow(10, -9);// time in nanoseconds

    printf(" PAGE FAULT RATE: ");
pg_fault_rate = (eff_access_time - mat) / (mod_percentage * modified_page + (1 - mod_percentage) * unmodified_pg - mat);
    printf("%lf", pg_fault_rate);

    return 0;
}
