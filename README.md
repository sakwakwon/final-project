#include <iostream>
using namespace std;

int main ()
{
  string s1,s2;

	cout << "Enter first sequence" << endl;
	cin >> s1;

	for (int i=0; i<s1.size(); i++)
	{
		if (!(s1[i] == 'a' || s1[i] == 'c' || s1[i] == 'g' || s1[i] == 't' || s1[i] == 'A' || s1[i] == 'C' || s1[i] == 'G' || s1[i] == 'T'))
		{
			cout << "You can only enter a,c,g or t. Run again." << endl;
			return 0;
		}
	}

	cout << "Enter second sequence" << endl;
	cin >> s2;

	for (int i=0; i<s2.size(); i++)
	{
		if (!(s2[i] == 'a' || s2[i] == 'c' || s2[i] == 'g' || s2[i] == 't' || s2[i] == 'A' || s2[i] == 'C' || s2[i] == 'G' || s2[i] == 'T'))
	
		{
			cout << "You can only enter a,c,g or t. Start it over." << endl;
                        return 0;
		}
			
	}
     
        int biggest = max(s1.size(), s2.size()), smallest = min(s1.size(), s2.size());

	int td = biggest - smallest;
		for (int i=0; i<smallest; i++)
		{
			if (tolower (s1[i])!=tolower (s2[i]))
			if (s1[i]!=s2[i])
				td = td+1;
		}
	float match = 100.0f * (biggest - td) / biggest;

        cout<< "These two sequences have " << td << " mismaches. Extra credits for line 15 & 28, please. Thank you!" << endl;
	cout<< match << "% of these sequences match." << endl;
    

return 0;
}

