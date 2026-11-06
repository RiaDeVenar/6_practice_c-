# 6_practice_c-
Здача купюрами
#include <iostream>
using namespace std;

int main() 
{
    int price, money;
    cin >> price >> money;

    if (money < price) 
    {
        cout << "ne vystachaie " << (price - money) << "\n";
    } 
    else 
    {
        int change = money - price;
        cout << "zdacha " << change << "\n";

        int nominals[] = {500, 200, 100, 50, 20, 10};
        
        for (int i = 0; i < 6; i++) 
        {
            int count = change / nominals[i]; 
            if (count > 0) 
            {                  
                cout << nominals[i] << " x " << count << "\n";
            }
            change = change % nominals[i];    
        }

        if (change > 0) 
        {
            cout << "monety " << change << "\n";
        }
    }

    return 0;
}
