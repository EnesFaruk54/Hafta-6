# Hafta-6
Hafta 6 Ödevim




#include <iostream>
#include <ctime>
using namespace std;
int main()
{
    int sayi;
    int tahmin = -1;
    int tahmin_sayisi = 0;
    int tahmin_limiti = 3;
    bool outOfGuesses = false;
    srand(time(NULL));

    sayi = rand() % 9 + 1;
    cout << sayi;
    while(tahmin != sayi && tahmin_sayisi < tahmin_limiti){
        cout << "Tahmininizi girin: ";
        cin >> tahmin;
        tahmin_sayisi++;
    }
    if(tahmin == sayi){
         cout << "Tebrikler, " << tahmin_sayisi <<". denemede kazandiniz!" << endl;
    } else {
         cout << "Uzgunum, 3 hakkinizda bilemediniz!" << endl;
    }
    return 0;
}

  
  
  #include <iostream>
using namespace std;
int main()
{
    int a[4][4] = {{1, 2, 3, 4},
                   {5, 6, 7, 8},
                   {9, 10, 11, 12},
                   {13, 14, 15, 16}};
    int m = 4, n = 4, i, j = 0, k = 0;
    while (k < m && j < n) {
        for (i = j; i < n; ++i) {
            cout << a[k][i] << " ";
        }
        k++;
        for (i = k; i < m; ++i) {
            cout << a[i][n - 1] << " ";
        }
        n--;
        if (k < m) {
            for (i = n - 1; i >= j; --i) {
                cout << a[m - 1][i] << " ";
            }
            m--;
        }
        if (j < n) {
            for (i = m - 1; i >= k; --i) {
                cout << a[i][j] << " ";
            }
            j++;
        }
    }
    return 0;
}
  
  
  
  #include <iostream>
using namespace std;
int main()
{
    int notlar[2][6] = {{85, 73, 92, 95, 80, 78},
                    {69, 76, 87, 65, 90, 50}};
    int top1 = 0, top2 = 0, n = 6;
    float ort1, ort2;
    cout << "Kimya Notlari: " << endl;
    for (int i=0; i < n; i++) {
        cout << notlar[0][i] << " ";
        top1 += notlar[0][i];
    }
    cout << "\nBiyoloji Notlari: " << endl;
    for (int i=0; i < n; i++) {
        cout << notlar[1][i] << " ";
        top2 += notlar[1][i];
    }
    ort1 = (float)top1 / n;
    cout << "\nKimya ortalamasi: " << ort1 << endl;
    ort2 = (float)top2 / n;
    cout << "\nBiyoloji ortalamasi: " << ort2 << endl;
    return 0;
}
