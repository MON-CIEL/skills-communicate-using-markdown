# Voici mon premier Header
## Voici mon deuxiéme Header
### Voici mon troisiéme Header
#### Voici mon quatriéme Header
##### Voici mon cinquiéme Header
###### Voici mon sixiéme Header

![image of Justicetocat](https://github.com/user-attachments/assets/ee70af81-b2d0-4999-9408-54254867b77b)

## VOici un programme permetant de calculer le cout de 2 abonnements telephonique en fonction du nombre de message et le temps d'appel en minute
```c++
#include <stdio.h> /* Lib Printf , Scanf*/
#include <stdlib.h> /* Lib Standard*/
#include <iostream> /* Lib Cin , Cout */
#include <string> /* Lib String */
#include <conio.h> /* Lib getch() */
#include <iomanip> /* Lib Set... , hex , dec , ...*/
using namespace std;

int main() {


	/*Formule A*/
	float const coutFormuleA(2.0);
	double const prixAppelFormuleA(0.3);
	double resultatPrixAppelFormuleA;
	double const prixSMSFormuleA(0.1);
	double resultatPrixSMSFormuleA;
	double coutTotalFormuleA;
	int coutRelatifAppelFormuleA;
	int coutRelatifSMSFormuleA;


	/*Formule B*/
	float const coutFormuleB(4.0);
	double const prixAppelFormuleB(0.2);
	double resultatPrixAppelFormuleB(0);
	double const prixSMSFormuleB(0.088);
	double resultatPrixSMSFormuleB;
	double coutTotalFormuleB;
	int coutRelatifAppelFormuleB;
	int coutRelatifSMSFormuleB;


	/* Donnée Saisit */
	int dureeAppel;
	int nombreSMS;

	/* Reccommencer */
	char ouiOuNon;
	bool reccommencerSyntaxe;
	bool reccommencer;

	/* Do principal permetant de recommencer tout le programme */
	do {

		cout << "Bonjour bienvenue dans mon programme , l'auteur de programme donc moi, est Marcelo MMG" << endl;
		cout << "\nVeuillez reinseigner une estamation de votre duree d'appel par mois\n" << endl;
		cout << "Valeur Saisie : ";
		cin >> dureeAppel;
		cout << "\nVeuillez reinseigner une estamation de votre nombre de message par mois\n" << endl;
		cout << "Valeur Saisie : ";
		cin >> nombreSMS;


		/* Calculs */
		resultatPrixAppelFormuleA = prixAppelFormuleA * dureeAppel;
		resultatPrixAppelFormuleB = prixAppelFormuleB * dureeAppel;
		resultatPrixSMSFormuleA = prixSMSFormuleA * nombreSMS;
		resultatPrixSMSFormuleB = prixSMSFormuleB * nombreSMS;
		coutTotalFormuleA = resultatPrixSMSFormuleA + resultatPrixAppelFormuleA + coutFormuleA;
		coutTotalFormuleB = resultatPrixSMSFormuleB + resultatPrixAppelFormuleB + coutFormuleB;
		coutRelatifAppelFormuleA = (resultatPrixAppelFormuleA / coutTotalFormuleA) * 100;
		coutRelatifSMSFormuleA = (resultatPrixSMSFormuleA / coutTotalFormuleA) * 100;
		coutRelatifAppelFormuleB = (resultatPrixAppelFormuleB / coutTotalFormuleB) * 100;
		coutRelatifSMSFormuleB = (resultatPrixSMSFormuleB / coutTotalFormuleB) * 100;


		/* Resultats */
		cout << "\nLe prix pour la formule A est de " << fixed << setprecision(2) << coutTotalFormuleA << " euros dont :\n" << endl;
		cout << "	" << fixed << setprecision(2) << resultatPrixAppelFormuleA << " euros pour la duree d'appel par mois saisie qui represente " << coutRelatifAppelFormuleA << "% du cout total" << endl;
		cout << "	" << fixed << setprecision(2) << resultatPrixSMSFormuleA << " euros pour le nombre de SMS par mois saisie qui represente " << coutRelatifSMSFormuleA << "% du cout total" << endl;
		cout << "	" << fixed << setprecision(2) << coutFormuleA << " euros pour le prix de l'abonnement de la formule A\n" << endl;


		cout << "\nLe prix pour la formule B est de " << fixed << setprecision(2) << coutTotalFormuleB << " euros dont :\n" << endl;
		cout << "	" << fixed << setprecision(2) << resultatPrixAppelFormuleB << " euros pour la duree d'appel par mois saisie qui represente " << coutRelatifAppelFormuleB << "% du cout total" << endl;
		cout << "	" << fixed << setprecision(2) << resultatPrixSMSFormuleB << " euros pour le nombre de SMS par mois saisie qui represente " << coutRelatifSMSFormuleB << "% du cout total" << endl;
		cout << "	" << fixed << setprecision(2) << coutFormuleB << " euros pour le prix de l'abonnement de la formule B\n" << endl;


		/*Tableau*/
		cout << "\nVoici un tableau ou les donnee sont resensees : \n" << endl;
		cout << setw(25) << "" << "-------------------------------------------------------" << endl;
		cout << setw(26) << "|" << setw(27) << "Formule A |" << setw(27) << "Formule B |" << endl;
		cout << "--------------------------------------------------------------------------------" << endl;
		cout << "|" << setw(25) << "Cout Appel |" << setw(25) << fixed << setprecision(2) << resultatPrixAppelFormuleA << " |" << setw(25) << fixed << setprecision(2) << resultatPrixAppelFormuleB << " |" << endl;
		cout << "--------------------------------------------------------------------------------" << endl;
		cout << "|" << setw(25) << "Cout SMS |" << setw(25) << fixed << setprecision(2) << resultatPrixSMSFormuleA << " |" << setw(25) << fixed << setprecision(2) << resultatPrixSMSFormuleB << " |" << endl;
		cout << "--------------------------------------------------------------------------------" << endl;
		cout << "|" << setw(25) << "Cout Formule |" << setw(25) << coutFormuleA << " |" << setw(25) << coutFormuleB << " |" << endl;
		cout << "--------------------------------------------------------------------------------" << endl;
		cout << "|" << setw(25) << "Cout Total |" << setw(25) << fixed << setprecision(2) << coutTotalFormuleA << " |" << setw(25) << fixed << setprecision(2) << coutTotalFormuleB << " |" << endl;
		cout << "--------------------------------------------------------------------------------" << endl;
		cout << "|" << setw(25) << "Cout Relatif Appel |" << setw(24) << coutRelatifAppelFormuleA << "% |" << setw(24) << coutRelatifAppelFormuleB << "% |" << endl;
		cout << "--------------------------------------------------------------------------------" << endl;
		cout << "|" << setw(25) << "Cout Relatif SMS |" << setw(24) << coutRelatifSMSFormuleA << "% |" << setw(24) << coutRelatifSMSFormuleB << "% |" << endl;
		cout << "--------------------------------------------------------------------------------" << endl;

		/*--------------------------------------------Reccommnecer----------------------------------------------*/

		/* Do secondraire permetant de recommencer tout le programme */
		do {
			cout << "\nVoulez vous recommnecer O/N\n" << endl;
			cin >> ouiOuNon;

			if (ouiOuNon == 'O') {

				reccommencer = true;
				reccommencerSyntaxe = false;
			}

			else if (ouiOuNon == 'N') {

				reccommencer = false;
				reccommencerSyntaxe = false;
			}

			else {

				reccommencer = false;
				reccommencerSyntaxe = true;
			}

		} while (reccommencerSyntaxe == true);


	} while (reccommencer == true);

}

```
















J'ai ajouté un code de mon choix
