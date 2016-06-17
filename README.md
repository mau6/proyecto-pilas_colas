                     proyecto.h para pila
#include <iostream>
#include <stdio.h>
#include <stdlib.h>

using namespace std;

struct pila {
	char caracter;
	pila * siguiente;
};

pila * inicio; pila * temp; pila * fin;

void insertar(char caracter2){
	if (inicio==NULL){
		inicio= new(pila);
		inicio->caracter=caracter2;
		fin=inicio;
	}else{
		temp=new(pila);
		temp->siguiente=inicio;
		temp->caracter=caracter2;
		inicio=temp;
	}
	fin->siguiente=NULL;
}

void mtodo(){
	temp= inicio;
	if(inicio==NULL){
		cout <<"No hay nada en pila" << endl;
	}else{
		while (temp != NULL ){
			cout <<temp->caracter<< endl;
			temp = temp->siguiente;
}
}
}

void top(){
	temp= inicio;
	if(inicio==NULL){
		cout <<"No hay nada en pila" << endl;
	}else{
		if(temp != NULL ){
			cout <<temp->caracter<< endl;
		}
	}
}


void elimina(){
	struct pila *pant=NULL;
	if (inicio==NULL){
		cout<<"No hay nada en pila" << endl;
	}
	else {
		temp=inicio;
		inicio=inicio->siguiente;
		pant=temp;
		pant->siguiente=temp->siguiente;
	}
}

void cantidad(){
	int contador=0;
	temp= inicio;
	if(inicio==NULL){
		cout <<"No hay nada en pila" << endl;
	}else{
		while (temp != NULL ){
            contador++;
			temp = temp->siguiente;
	}
	cout<<"Nodos  "<<contador<<endl;
}
}



                           proyecto.h para cola
  #include <iostream>
#include <stdio.h>
#include <stdlib.h>
using namespace std;


struct cola {
	char caracter;
	cola * siguiente;
};

cola * prin; cola * tempo; cola * final;

void push(char caracter2){
	if (prin==NULL){
		prin= new(cola);
		prin->caracter=caracter2;
		final=prin;
	}else{
		tempo=new(cola);
		final->siguiente=tempo;
		tempo->caracter=caracter2;
		final=tempo;
	}
	final->siguiente=NULL;
}

void muestrat(){
	tempo= prin;
	if(prin==NULL){
		cout <<"No hay nodos encolados" << endl;
	}else{
		while (tempo != NULL ){
			cout <<tempo->caracter<< endl;
			tempo = tempo->siguiente;
	}
}
}

void Top(){
	tempo= prin;
	if(prin==NULL){
		cout <<"No hay nodos encolados" << endl;
	}else{
		if(tempo != NULL ){
			cout <<tempo->caracter<< endl;
		}
	}
}

void pop(){
	struct cola *pant=NULL;
	if (prin==NULL){
		cout<<"No hay nodos encolados" << endl;
	}
	else {
		tempo=prin;
		prin=prin->siguiente;
		pant=tempo;
		pant->siguiente=tempo->siguiente;
	}
}

void numnodo(){
	int contador=0;
	tempo= prin;
	if(prin==NULL){
		cout <<"No hay nodos encolados" << endl;
	}else{
		while (tempo != NULL ){
            contador++;

			tempo = tempo->siguiente;
	}
	cout<<"Nodos   "<<contador<<endl;
}
}


                        archivo.cpp
  //============================================================================
// Name        : proyecto.cpp
// Author      : maury alvarado
// Version     :
// Copyright   : Your copyright notice
// Description : Hello World in C++, Ansi-style
//============================================================================

#include <iostream>
#include "pila.h"
#include "cola.h"
using namespace std;

int main() {
	            //funciones de pila
//insertar: agrega un nodo 
//mtodo: muestra todo los nodos ingresados
//top: muestra el nodo que se va a eliminar
//elimina: elimina el nodo segun regla
//cantidad: indica el numero de nodos ingresados
	
	
	 	 	 	 //funciones de cola
//push: agrega un nodo
//muestrat: muestra todo los nodos ingresados
//Top: muestra el nodo que se va a eliminar
//pop: elimina el nodo segun regla
//numnodo: indica el numero de nodos ingresados

	return 0;
}
