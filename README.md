#include<iostream>
using namespace std;

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
                default:
                cout<<"INVALID"<<endl;
                break;
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
                default:
                cout<<"INVALID"<<endl;
                break;
            }
        }
    }
    
    

};


int main(){
    
    converter<float, float>obj(89.95);
    obj.show();
    
    
    return 0;
}
