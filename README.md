Questão 1: 

#include <iostream>
#include <iomanip>

using namespace std;

int main() {
    int qtd;
    cin >> qtd;

    float preco = (qtd >= 12) ? 0.65 : 0.80;
    float total = preco * qtd;

    cout << fixed << setprecision(2);
    cout << "Preco da unidade: R$" << preco << endl;
    cout << "Preco total: R$" << total << endl;

    return 0;
}


Questão 2: 

#include <iostream>

using namespace std;

int main() {
    int num;
    cin >> num;

    if (num < 0 || num > 50) {
        cout << "Valor invalido!" << endl;
        return 0;
    }

    for (int i = num - 1; i > 0; i--) {
        cout << "Resto da divisao de " << num << " por " << i << ": " << num % i << endl;
    }

    return 0;
}


Questão 3: 

#include <iostream>

using namespace std;

int main() {
    int n;
    cin >> n;  // número de testes

    for (int t = 0; t < n; t++) {
        int pares = 0, impares = 0, positivos = 0, negativos = 0;
        for (int i = 0; i < 5; i++) {
            int num;
            cin >> num;

            if (num % 2 == 0) pares++;
            else impares++;

            if (num > 0) positivos++;
            else if (num < 0) negativos++;
        }

        cout << "Quantidade de numeros pares: " << pares << endl;
        cout << "Quantidade de numeros impares: " << impares << endl;
        cout << "Quantidade de numeros positivos: " << positivos << endl;
        cout << "Quantidade de numeros negativos: " << negativos << endl;
        cout << endl;  // separa a saída dos testes
    }

    return 0;
}
