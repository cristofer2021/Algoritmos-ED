# Algoritmos-ED
#include <stdio.h>
#include <string.h>
//DECLARACION DE VARIABLES
int ma, num, pe, tot,pes, peso;
  int aux=1;
  int aux1=1;
  int aux2=1;
  char an[20];
  char op;
//FUNCIÓN PRINCIPAL
int main() {
  do {
    printf("MENU\n");
    printf("a) Mamíferos\nb) Reptiles\nc) Aves\nd) Número de animales y peso total\ne) Salir\nOPCIÓN: ");
    scanf("%s", &op);
    switch(op){
      case 'A':
      case 'a':{
      printf("¿Cuantos animales mamíferos ingresaran?\n");
      scanf("%d", &ma);

      do {
        printf("Mamífero %d\n", aux);
        printf("¿De qué animal se trata?\n");
        scanf("%s", an);
        printf("¿Cuantos %ss ingresarán\n", an);
        scanf("%d", &num);
        printf("Peso de cada %s en kg\n", an);
        scanf("%d", &pe);
        aux++;
        tot=tot+num;
        pes=num*pe;
        peso=peso+pes;
        } while(ma>=aux);
      }break;
        case 'B':
        case 'b':{
        printf("¿Cuantos animales reptíles ingresaran?\n");
      scanf("%d", &ma);
      do {
        printf("Reptiles %d\n", aux1);
        printf("¿De qué animal se trata?\n");
        scanf("%s", an);
        printf("¿Cuantos %ss ingresarán\n", an);
        scanf("%d", &num);
        printf("Peso de cada %s en kg\n", an);
        scanf("%d", &pe);
        tot=tot+num;
        aux1++;
        pes=num*pe;
        peso=peso+pes;
      } while(ma>=aux1);
        }break;
        case 'C':
        case 'c':{
        printf("¿Cuantos animales aves ingresaran?\n");
      scanf("%d", &ma);
      do {
        printf("Aves %d\n", aux2);
        printf("¿De qué animal se trata?\n");
        scanf("%s", an);
        printf("¿Cuantos %ss ingresarán\n", an);
        scanf("%d", &num);
        printf("Peso de cada %s en kg\n", an);
        scanf("%d", &pe);
        aux2++;
        tot=tot+num;
        pes=num*pe;
        peso=peso+pes;
      }while(ma>=aux2) ;
      }break;
      case 'D':
      case 'd':
      printf("Se han ingresado %d animales, con un peso total de %d kg\n", tot, peso);
      break;
      case 'E':
      case 'e':
      printf("\n\t\t\t\t\t¡¡¡¡¡ATENCIÓN!!!!!\n\n\n¡Gracias por su atención!");
    }
    } while(op!='e'&& op!='E' );
  return 0;
}
