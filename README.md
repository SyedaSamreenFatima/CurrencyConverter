#include<iostream>
using namespace std;

template <class t, class s>
class converter{
    protected:
    t amount;

    public:

    converter(t amo){
        amount = amo;

    }

    void show(){

        char option, posession;

        cout<<"LIST :"<<endl;
        cout<<"a. BDT"<<endl;
        cout<<"b. AFN"<<endl;
        cout<<"c. PKR"<<endl;
        cout<<"d. INR"<<endl;
        cout<<"e. NPR"<<endl;
        cout<<"f. LKR"<<endl;

        cout<<"Your Currency?  : ";
        cin>>posession;

        cout<<"Enter Currency for conversion : ";
        cin>>option;

        if(posession == 'a')
        {
            switch(option)
            {
                case 'a':
                cout<<"INVALID"<<endl;
                break;
                case 'b':
                cout<<"BDT to AFN = "<<amount*0.66<<" AFN"<<endl;
                break;
                
                break;
                case 'c':
                cout<<"BDT to PKR = "<<amount*2.54<<" PKR"<<endl;
                break;
                case 'd':
                cout<<"BDT to INR = "<<amount*0.76<<" INR"<<endl;
                break;
                case 'e':
                cout<<"BDT to NPR = "<<amount*1.22<<" NPR"<<endl;
                break;
                case 'f':
                cout<<"BDT to LKR = "<<amount*2.7<<" LKR"<<endl;
                break;
                default:
                cout<<"INVALID"<<endl;
            }
        }

        else if(posession == 'b')
        {
            switch(option)
            {
                case 'b':
                cout<<"INVALID"<<endl;
                break;
                case 'a':
                cout<<"AFN to BDT = "<<amount/0.66<<" BDT"<<endl;
                break;
               
                case 'c':
                cout<<"AFN to PKR = "<<amount*3.86<<" PKR"<<endl;
                break;
                case 'd':
                cout<<"AFN to INR = "<<amount*1.15<<" INR"<<endl;
                break;
                case 'e':
                cout<<"AFN to NPR = "<<amount*1.85<<" NPR"<<endl;
                break;
                case 'f':
                cout<<"AFN to LKR = "<<amount*4.1<<" LKR"<<endl;
                break;
                default:
                cout<<"INVALID"<<endl;
            }
        }
    }



};


int main(){

    converter<float, float>obj(89.95);
    obj.show();


    return 0;
}
