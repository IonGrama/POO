# POO
#include <iostream>
using namespace std;

class student
{
public:
    string nume;
    int an;
    int nota;
    int n;
public : student()
    {
        nume = "";
        an = 0;
    nota=0;
    }
public : student(char n,int an,int nota)
    {
        nume = n;
        an = an;
     nota=nota;
    }
 public: void Citeste_ST()
    {
        cout<<"\n\t\tNume:";
        cin>>nume;
        cout<<"\n\t\tAnul:";
        cin>>an;
        cout<<"\n\t\tNota:";
        cin>>nota;
    }
    //Functia de afisare a datelor
    public: void Afisare_ST()
    {
        cout<<"\n\t--------------------------";
        cout<<"\n\t\tNume"<<nume;
        cout<<"\n\t\tAnul:"<<an;
        cout<<"\n\t\tNota:"<<nota;
        cout<<"\n\t--------------------------";
    }
  public:
    int Media(){
        return nota*50/10;
    }
};


class Universitate : student

{
public:
    string Nume;
    int An;
    int n;

    public : Universitate()
    {
        Nume = " ";
        An = 0;
    }

public:
    Universitate(string univer, int an)
    {
        Nume = univer;
        An = an;
    }

public:
    void Citeste()
    {
        cout << "\t\nIntroduceti datele:";
        cout << "\nNume universitate:";
        cin >> Nume;
        cout << "\nAnul fondarii:";
        cin >> An;
        cout << "\nIntrodu numarul total de studenti: ";
        cin >> n;

    }

public:
    void Afiseaza()
    {
        cout << "\nAfisarea datelor:";
        cout << "\nNume universitate:" << Nume;
        cout << "\nAnul Fondarii:" << An;
    }

};

int main()
{

    Universitate u[5];
    student st[5];
    int n,m;
    cout<<"\n\tIntroduceti numarul de studenti:";
    cin>>n;
    for(int i=0;i<n;i++){
        cout<<"\n\tIntroduceti datele :";
        st[i].Citeste_ST();
    }
    for(int i=0;i<n;i++){
        cout<<"\n\tAfisarea datele:";
        st[i].Afisare_ST();
         cout<<"\n\tMedia:";
        st[i].Media();
    }
    cout<<"\n\tIntroduceti numarul de Universitati:";
    cin>>m;
    for(int j=0;j<m;j++){
        cout<<"\n\tIntroduceti datele :";
        u[j].Citeste();
    }
    for(int j=0;j<m;j++){
        cout<<"\n\tAfisarea datele:";
        u[j].Afiseaza();
    }
    return 0;
}
