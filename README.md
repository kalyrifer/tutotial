#include<cmath>
#include <iostream>
#include<ctime>
#include<iomanip>
using namespace std;

int main() {
    setlocale(LC_ALL, "Russian");


    char mart[99][99];
    cout << "введите n" << endl;
    int n;
    cin >> n;
    cout << endl;

    int k = n;


    // заполняем матрицу 
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            mart[i][j] =( rand() % 20)+38;
        }
    }
    cout << "начальная матрица" << endl;
    //выводим матрицу
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cout << mart[i][j] << "    ";
        }
        cout << endl << endl;
    }
    //заполнение а
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            if (i < j) {
                if (mart[i][j] < 48) {
                    mart[i][j] = 97;

                }
            }
        }
    }
    cout <<endl<< "новая матрица" << endl;

    //выводим матрицу
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            cout << mart[i][j] << "    ";
        }
        cout << endl << endl;
    }
}
