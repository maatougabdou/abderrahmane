#include<stdio.h>
int main(){
int n,i;
printf("donne n:");
scanf("%d",&n);
int est_premier = 1;
for(i = 2;i <= n/2;i++){
    if(n % i ==0){
        est_premier = 0;
    }
}
if(est_premier ==1){
    printf("le plue petit diviseur est:1\nle plue grand diviseur est: %d\n",n);
}else{
    int ppd= 1;
    int pgd= 1;
 for(i = 2;i <= n/2;i++){
    if(n % i ==0){
        ppd = i;
    }
 }
 for(i = n/2;i >= 2;i--){
    if(n % i ==0){
        pgd = i;
    }
 }
 if(ppd == pgd){
    printf("le plue petit diviseur =le plue grand diviseur =%d",i);
 }else{
    printf("le plue petit diviseur est:%d\n,le plue grand diviseur est: %d\n",ppd,pgd);
 }
}
return 0;
