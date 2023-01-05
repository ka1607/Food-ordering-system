#include <iostream>
using namespace std;
int main()
        {
            cout<<"-----------------------INDIAN FOOD----------------------\n";
            cout<<"__________________________________________________________\n";
            cout<<"----------------------------------------------------------\n";
            cout<<"                        Token | Price                                  Token | Price\n";
            cout<<"GRAVY                                              BREADS\n";
            cout<<"`````                                              ``````\n";
            cout<<"Veg\n\n";
            cout<<"1. Shahi Paneer             1 | 240                1. Tandoori Roti       21 | 25\n";
              cout<<"2. Mutter Mushroom          2 | 220                2. Lacha Paratha       22 | 40\n";
            cout<<"3. Dal Makhani              3 | 180                3. Missi Roti          23 | 50\n";
              cout<<"4. Malai Kofta              4 | 230                4. Butter Naan          24 | 30\n";
                cout<<"5. Palak Paneer             5 | 200                5. Rumali Roti          25 | 25\n\n\n";
                cout<<"Non-Veg                                            DESERTS";
                cout<<"                                                                         ```````\n";
                cout<<"1. Mutton Do Pyaza          6 | 440                1. Ice Cream           26 | 80\n";
                cout<<"2. Butter Chicken           7 | 400                2. Gulab Jamun         27 | 90 \n";
                cout<<"3. Chilli Chicken           8 | 420                3. Rasmalai            28 | 100\n";
                cout<<"4. Patiala Chicken          9 | 390                4. Jalebi Rabdi        29 | 120\n";
                cout<<"5. Mutton Rogan Josh       10 | 500                5. Gajar Halwa         30 | 70\n\n";
                cout<<"SNACKS                                             DRINKS  \n";
            cout<<"``````                                             ``````\n";
            cout<<"Veg\n";
             cout<<"1. French Fries            11 | 100                1. Tea                 31 | 20\n";
             cout<<"2. Paneer Tikka            12 | 250                2. Coffee(hot/cold)    32 | 50\n";
             cout<<"3. Paneer Pakoda           13 | 200                3. Green Tea           33 | 60\n";
             cout<<"4. Dry Manchurian          14 | 160                4. Cold Drink          34 | 40\n";
             cout<<"5. Chilli Potato           15 | 200                5. Water Bottle        35 | 20\n";
             cout<<"Non-Veg                                            6. Vanilla Shake       36 | 100\n";
             cout<<"1. Tandoori Chicken        16 | 400                7. Choclate Shake      37 | 100\n";
             cout<<"2. Afgani Chicken          17 | 360                8. Strawberry Shake    38 | 100\n";
             cout<<"3. Fried Chicken           18 | 380                9. Banana Shake        39 | 100\n";
             cout<<"4. Seekh Kebab             19 | 400                10. Mango Shake        40 | 100\n";
             cout<<"5. Chicken Tikka           20 | 380\n\n";
             string menu[40]={"Shahi Paneer","Mutter Mushroom","Dal Makhani","Malai Kofta","Palak Paneer","Mutton Do Pyaza","Butter Chicken","Chilli Chicken","Patiala Chicken","Mutton Rogan Josh","French Fries","Paneer Tikka","Paneer Pakoda","Dry Manchurian","Chilli Potato","Tandoori Chicken","Afgani Chicken","Fried Chicken","Seekh Kebab","Chicken Tikka","Tandoori Roti","Lacha Paratha","Missi Roti","Butter Naan","Rumali Roti","Ice Cream","Gulab Jamun","Rasmalai","Jalebi rabdi","Gajar Halwa","Tea","Coffee","Green Tea","Cold Drink","Water Bottle","Vanilla Shake","Choclate Shake","Strawberry Shake","Banana Shake","Mango Shake"};
    int price[40]={240,220,180,230,200,440,400,420,390,500,100,250,200,160,200,400,360,380,400,380,25,40,50,30,25,80,90,100,120,70,20,50,60,40,20,100,100,100,100,100};
    int q[40]={0};
    int t;
    int sum=0;
    while(1)
    {
        cout<<"Enter item's token and its quantity\nEnter 50 if your order is complete"<<endl;
        cout<<"Token=";
        cin>>t;
        if(t==50)
        break;
        cout<<"Quantity=";
        cin>>q[t];
        sum=sum+q[t+1]*price[t+1];
    }
    cout<<sum;
    cout<<"          BILL"<<endl;
    cout<<"Sr.No\t"<<"Item\t\t"<<"Quantity\t"<<"Price\t"<<endl;
    int ii=1;
    for(int i=0;i<40;i++)
    {
     if(q[i])
     {
        cout<<ii<<'\t'<<menu[i]<<'\t'<<q[i]<<'\t'<<'\t'<<q[i]<<"*"<<price[i]<<"="<<q[i]*price[i]<<endl;
     }
    }
    cout<<"Total Amount is : "<<sum<<endl;
    return 0;
}
