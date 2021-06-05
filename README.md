#include <iostream>
using namespace std;
void Mayor_Menor ()
{
	int vector[50];
	int i,j,aux;
	
	
	for (i=0;i<9;i++)
	{
		for(j=i+1;j<9;j++)
		{
			if (vector[i]<vector[j])
			{
				aux=vector[i];
				vector[i]=vector[j];
				vector[j]=aux;
			}
		}
	}
	
	cout<<"\nVector ordenado de mayor a menor ";
	
	for (i=0;i<9;i++)
	{
		cout<<vector[i]<<",";
	}
	
	
}
void Menor_Mayor ()
{
	int vector[50];
	int i,j,aux;
	
	
	for (i=0;i<9;i++)
	{
		for(j=i+1;j<9;j++)
		{
			if (vector[i]>vector[j])
			{
				aux=vector[i];
				vector[i]=vector[j];
				vector[j]=aux;
			}
		}
	}
	
	cout<<"\nVector ordenado de menor a mayor ";
	
	for (i=0;i<9;i++)
	{
		cout<<vector[i]<<",";
	}
	
}
void Pares()
{
	int numeros[10], *dir_numero;
	
	dir_numero = numeros;
	for(int i=0;i<10;i++){
		if(*dir_numero%2==0){
			cout<<"El numero "<<*dir_numero<<" es par"<<endl;
		}
		dir_numero++;
	}
	
}
void Impares()
{
	int numeros[10], *dir_numero;
	
	dir_numero = numeros;
	for(int i=0;i<10;i++){
		if(*dir_numero%2!=0){
			cout<<"El numero "<<*dir_numero<<" es impar"<<endl;
		}
		dir_numero++;
	}
	
}
void Lista()
{
	int numeros[10], *dir_numero;
	
	dir_numero = numeros;
	for(int i=0;i<10;i++){
		if(*dir_numero%2!=0 || *dir_numero%2==0){
			cout<<"El numero "<<*dir_numero<<endl;
		}
		dir_numero++;
	}
	
}

int main(int argc, char *argv[]) {
	int respuesta =0;
	int vector[50];
	int i,j,aux;
	do{
		cout<<"Digite los valores"<<endl;
		for (i=0;i<9;i++)
		{
			cout<<"X["<<(i+1)<<"]= ";
			cin>>vector[i];
		}
		cout<<"Que desea hacer"<<endl;
		cout<<"1- Ordenar de Mayor a Menor"<<endl;
		cout<<"2- Ordenar de menor a mayor"<<endl;
		cout<<"3- Elementos pares de la lista"<<endl;
		cout<<"4- Elementos impares de la lista"<<endl;
		cout<<"5- Todos los elementos de la lista"<<endl;
		cin>>respuesta;
		if (respuesta == 1){
			Mayor_Menor();
		}
		else{
			if (respuesta == 2){
				Menor_Mayor();
			}
			else{
				if (respuesta == 3){
					Pares();
				}
				else{ if (respuesta == 4){
					Impares();
				}
				else{ if (respuesta == 5){
					Lista();
				}
				}
				}
			}
		}
	}while(respuesta != 0);
	return 0;
}
