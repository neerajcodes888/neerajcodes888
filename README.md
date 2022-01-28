#include<iostream>
#include<iomanip>
#include<Windows.h>
using namespace std;
class stack
{
	int size=8,top=-1;
	int s[8];
	public:
	void push()
	{
		if(top==size-1)
		{
			cout<<"Stack overflow";
		}
		else
		{
			int e;
			cout<<"Enter an element to push:";
			cin>>e;
			top++;
			s[top]=e;
			cout<<s[top]<<" inserted into the Stack";
		}
	}
	void pop()
	{
		if(top==-1)
		{
			cout<<"Stack underflow";
		}
		else
		{
			cout<<s[top]<<" removed from stack";
			top--;
		}
	}
	void display()
	{
		if(top>=0)
		{
			cout<<"--------------------------------------------------------------------------------------------"<<endl;
			cout<<"Stack elements:";
			for(int i=top;i>=0;i--)
			{
				cout<<s[i]<<" ";
			}
			cout<<endl<<"-------------------------------------------------------------------------------------------";
		}
	}
};
int main()
{
	int ch;
	class stack s;
		system("color b4");
		do
	{
	cout<<setw(100)<<endl<<"\t\t*****************************************Stack Menu******************************"<<endl;
	cout<<setw(65)<<"1).Push element"<<endl;
	cout<<setw(64)<<"2).Pop element"<<endl;
	cout<<setw(70)<<"3).Display the Stack"<<endl;
	cout<<setw(66)<<"4).Exit the menu"<<endl;
    cout<<setw(100)<<"\t\t***********************************************************************************";

		
		cout<<endl<<"Enter Your choice:";
		cin>>ch;
		system("cls");
		switch(ch)
		{	
			case 1:
			
			s.push();
			break;
			case 2:
			
			s.pop();
			break;
			case 3:
				
			s.display();
			break;
			case 4:
				cout<<"Exiting....";
				Sleep(1500);
				cout<<"exited";
				exit(0);
				
			break;
			default:
			
			cout<<"Invalid choice";
		}
	}while(ch!=4);
	return 0;
}
