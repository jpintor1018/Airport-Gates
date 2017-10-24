# Airport-Gates







#include <iostream> 
using namespace std;

int main()

{
	int arr[10], dep[10];
	int num, i, g;


	cout << " Enter Number of Flights " << endl;
	cin >> num;

		for ( i = 0; i < num ; i++)
			{
				cout << " Enter Arrival time " << endl;
				cin >> arr[i]; 

				cout << " Enter Departure time " << endl;
				cin >> dep[i];	
			}
			cout<<endl;

		cout << " Arrival Times : " << " " << " Departing Times : " << endl;

		for (i = 0; i < num ; i++)
			{
		 		cout << "    " << arr[i] << "			" << dep[i] << endl;
			}

			cout<<endl;
			

	int gateO=1, gateC=0;

		for ( i = 0; i < num; i++ )
			{
				for(  g= 0; g<i ; g++)
					{
						if (arr[i] < dep[g])
							gateO++;
						else
							gateC--;
							g++;
					}			 
				if (gateC > gateO)
					gateO++;	

			}

	cout << " Number of gates required to be open : " << gateO << endl;
	cout<<endl;

			
	

return 0; 		
}


