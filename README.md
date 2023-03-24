
#include <stdio.h>
#include <stdlib.h>
#define MAX_PILHA_SIZE 10


typedef struct {
    int dados [MAX_PILHA_SIZE];
    int Topo;

}XPILHA;

void XPILHA_INICIA(XPILHA *pilh){
    pilh-> Topo = -1;}

    int XPILHA_VAZIA (XPILHA *pilh){
    if (pilh->Topo == -1){
        return 1;}
        else{
            return 0;
        }
    }
    int XPILHA_CHEIA(XPILHA *pilh)
    {
    if (pilh->Topo == MAX_PILHA_SIZE -1){
        return 1;
    } else{
            return 0;}

        }
    int XPILHA_INSERE(XPILHA *pilh, int x){
    if(XPILHA_CHEIA (pilh) == 1) {
        printf ("a pilha está cheia");}
         else {

        pilh->Topo++;
        pilh->dados[pilh->Topo] = x;

    }}

     int XPILHA_RETIRA(XPILHA *pilh){
         int pxx;
    if(XPILHA_VAZIA (pilh) == 1) {
        printf ("a pilha está vazia");}
         else {

        pxx = pilh->dados[pilh->Topo];
        pilh->Topo--;
   }     return pxx;}



int main(){
     XPILHA *pilh= ( XPILHA*)malloc(sizeof( XPILHA));
      XPILHA_INICIA(pilh);

       XPILHA_INSERE(pilh, 3);
       XPILHA_INSERE(pilh, 4);
       XPILHA_INSERE(pilh, 5);
       int pxx;

        pxx = XPILHA_RETIRA(pilh);
       printf("\nfoi retirado %d", pxx);

       pxx = XPILHA_RETIRA(pilh);
       printf("\nfoi retirado %d", pxx);

        pxx = XPILHA_RETIRA(pilh);
       printf("\nfoi retirado %d", pxx);

       return 0;


}
