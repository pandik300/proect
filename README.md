#include <iostream>
#include <fstream>

using namespace std;

int main()
{
    setlocale(LC_ALL, "russian");
    int choise, a, b, c, max, min;
    ifstream fin("input.txt");
    fin >> a >> b >> c;
    fin.close();
    do
    {
        cout << "1 = нахождение наибольшего эелемента, 2 - нахождение наименьшего элемента, 3 - сумма элементов, 4 - произведение элементов, 0 - выход" << endl;
        cout << "Сделайте выбор" << endl;
        cin >> choise;
        switch(choise)
        {
            case 1: max = a;
                    if (b > max) max = b;
                    if (c > max) max = c;
                    cout << "наибольший элемент: " << max << endl;
                    break;
            case 2: min = a;
                    if (b < min) min = b;
                    if (c < min) min = c;
                    cout << "Наименьший элемент: " << min << endl;
                    break;
            case 3: cout << "Ответ: " << a + b + c << endl;
                    break;
            case 4: cout << "Ответ: " << a * b * c << endl;
                    break;
            case 0: break;
            default: cout << "ошибка"<< endl;

      }
    }
    while(choise);
    cout << "До свидания";
    return 0;
}
