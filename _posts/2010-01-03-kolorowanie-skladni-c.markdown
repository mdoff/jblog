---
layout: post
title: Kolorwanie skladni C
---
# {{ page.title }}

## Mały test kolorowania składni 
{% highlight c %}
#include <stdio.h>
#define LE  3

int por(float g[],float h[],int len){ /*funkca porownuje 2 tablice, jesli sa rowne zwraca 0 */
  int i2=0;                            /*jesli pierwsza jest wieksza to zwraca 1  */
  for(i2=0;i2<len;i2++){                 /*jesli druga jest wieksza to zwraca 2     */
    if (g[i2]!=h[i2]){                  /*zmienna len okresla dlugosc tych tablic */
      if(g[i2]>h[i2]){
	return 1;
      }
      else{
	return 2;
      }
    }
  }
  return 0;
}
	

int main(){

  int c,g,w,licznik;
  int t=0;
  /* printf("podaj dlugosc tablic: ");
     scanf("%d",&i); */
  float a[LE];
  float b[LE];

  printf("podaj liczbe tablic: ");
  scanf("%d",&t);

  printf("podaj pierwsza tablice: ");
  for (c=0;c<LE;c++){ /*wczytanie pierwszej tablicy */
    scanf("%f",&a[c]);
  }
  t--;

  for (g=1;g<=t;g++){
    
    printf("podaj %d tablice: ",g+1);
      for (c=0;c<LE;c++){
	scanf("%f",&b[c]);
      }
      w = por(a,b,LE); /*porownanie tablic */
      if(w == 2){  /*jesli tablica druga jest wieksza od pierwszej nastepuje jej przepisanie */
	for(licznik=0;licznik<LE;licznik++){
	  a[licznik] = b[licznik];
	} 
      }
      /*      printf("wynik to %d\n",w); */

  }
  printf("a zwyciezka tablica jest: \n");
  for (c=0;c<LE;c++){ /*drukowanie najwiekszej tablicy */
    printf("%f | ",a[c]);
  }
  printf("\n");
  return 0;
}

{% endhighlight %}

Jakieś zadanko ze wstępu do programowania
