#include <iostream>
using namespace std;
int main()
{
    int month=3, cnt, accNum;
    double  s_balance, dep, c_balance, withdr, endbalance, annualRate, monthRate, total_interest, avg_month, avg_total, total_balance;

    cout<<"\t \t \t  Welcome to Vikro \n \t \t \t The whole world in one bank"<<endl;
    cout<<"Enter your account number \t";
    cin>>accNum;

   cout<<" Please Enter your starting Balance \t";
   cin>>s_balance;
   cout<<"Enter your annual interest rate %";
   cin>>annualRate;
   annualRate=annualRate/100;
for (s_balance=+s_balance; s_balance>0;)
{


for (cnt =1; cnt<=month; cnt++)
{
s_balance=s_balance+total_balance;
    cout<<"Enter the total of deposits done over this month \t";
    cin>>dep;

    while (dep<0)
    {
        cout<<"FAILED: Please enter an amount greater than 0 \n";
        cin>>dep;
    }
    c_balance=s_balance+dep;
     cout<<"Enter the total of withdrawals done over this month \t";
     cin>>withdr;



     while (withdr<0 || withdr> c_balance)
     {
         cout<<"FAILED: The amount of money withdrawn cannot be greater than your balance. TRY AGAIN"<<endl;
        cin>>withdr;
     }

    endbalance=c_balance-withdr;
    avg_month=(endbalance+s_balance)/2;
    monthRate=annualRate/12;
    avg_total=avg_month*monthRate;
    total_balance=endbalance+avg_total;

cout<<"Your new balance is \t $"<<total_balance<<endl;



}
}
cout<<"Your initial starting balance \t $"<<s_balance<<endl;
cout<<"Total amount of deposits over the three months period \t $"<<dep<<endl;
cout<<"Total amount withdrawn over the three months period \t $"<<withdr<<endl;
cout<<"Total Interest collected over the three months period \t $"<<avg_total<<endl;
cout<<"\t \t \t Thanks for your loyalty \t \t \t"<<endl;



    return 0;
}

