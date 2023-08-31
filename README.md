
#include <bits/stdc++.h>
using namespace std;

class Calculator{
public:
	virtual void add (int x,y)=0;
	virtual void sub(int x, y)=0;
};
class doshtakarcal:public Calculator{
	public:
		void add (int x, y){
			cout << "Add : "<<x+y <<endl;
		}
		void sub (int x,  y){
			cout << "Sub : "<<x - y <<endl;
		}
};
class ekshotakarcal :public Calculator{
public:
		void add (int x, y){
			cout << "Add : "<<x+y <<endl;
		}
		void sub (int x, y){
			if (x>y){
				cout << "Sub : "<<x - y <<endl;
			}else{
				cout << "Sub : "<<y-x <<endl;
			}

		}
};

int main (){
	Calculator *c = new doshtakarcal();
	Calculator *c1 = new ekshotakarcal();
	c1->add(50,20);
	c1->sub(70,100);
}

