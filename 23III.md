<b> PĘTLE WARUNKOWE </b><br><br>
<b>
Zad 1<br>
Napisz program liczący pierwiastki trójmianu kwadratowego ax^2+bx+c=0</b><br>
pętla while dla pozbycia się przypadku a=0, czyli braku trójmianu kwadratowego 
```c
#include <stdio.h>
#include <math.h>
int main() {
double a=0,b=0,c=0, d, x ,x1, x2;
printf("podaj wspolczyniki trojmianu kwadratowego  ax^2+bx+c, \n");
scanf("%lf %lf %lf" , &a, &b, &c);
while (a==0){
printf("podaj a rozne od zera, \n");
scanf ("%lf" , &a);
}
d=(b*b)-(4*a*c);
    if (d>0){
    x1=((-b)-(sqrt(d)))/(2*a);
    x2=((-b)+(sqrt(d)))/(2*a);
    printf("pierwiastek  x1 = %lf\n", x1);
    printf("pierwiastek  x2 = %lf", x2);
    }
    else {if (d==0){
        x=(-b)/(2*a);
        printf("pierwiastek  x1=x2= %lf", x);
        }
        else 
        printf("brak pierwiastkow rzeczywistych");
        }
getchar(), getchar() ;
}
```
<b>Zad 2<br>
Znajdź liczby o tej własności, że suma dzielników właściwych liczby jest równa zadanej liczbie, np. 6=1+2+3. Są to tzw. liczby doskonałe.</b>
```c
#include <stdio.h>
#include <math.h>
int main() {
int i,s,n;
for (n=2; n<10000; n++){
    s=0;
    for(i=1; i<n; i++){
         if (n%i==0){
         s=s+i;
             }
    }
    if(s==n)
             printf("%d \n" , n);
}
getchar(), getchar() ;
return 0;
}
```
<b>Zad 3<br>
Wyświetl 20 róznych (bez permutacji) trójek pitagorejskich, tzn. takich liczb całkowitych dodatnich a, b, c, że a^2+b^2=c^2</b>


```c
#include <stdio.h>
#include <math.h>
int main(){
    int a,b,c,i;
    i=1;
   
    for(c=1; c<=100; c++){ 
             for(b=1; b<c; b++)
                      for(a=1; a<b; a++){
                               if (a*a+b*b==c*c && i<=20){
             printf("%d %d %d\n",a,b,c);
           i++;
               } 
             }
             }
                  
          getchar(),getchar();
          return 0;
}
```

```c
#include <stdio.h>
#include <math.h>
int main(){
    double zero=0.0;
    double max=-1/zero; 
    double min=1/zero; 
    double x;
    int n, i;
    printf("podaj ilosc liczb n:");
    scanf("%d", &n);
  
    for(i=1; i<=n; i++){
    printf("podaj liczbe");
    scanf("%lf", &x);
    if (x<max){        
    printf("najwieksza %5.5lf\n",max);
    }
    else { 
         printf("najwieksza %5.5lf\n",x);
        max=x;
         }
            if (x>min){        
    printf("najmniejsza %5.5lf\n",min);
    }
    else { 
         printf("najmniejsza %5.5lf\n",x);
        min=x;
         }
          }      
          getchar(),getchar();
          return 0;
}
```
