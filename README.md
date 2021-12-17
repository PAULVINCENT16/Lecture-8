# Lecture-8
//Days of the Month #include using namespace std;

int main() {

int date;
cout << "Press 1: January" << endl;
cout << "Press 2: February" << endl;
cout << "Press 3: March" << endl;
cout << "Press 4: April" << endl;
cout << "Press 5: May" << endl;
cout << "Press 6: June" << endl;
cout << "Press 7: July" << endl;
cout << "Press 8: August" << endl;
cout << "Press 9: September" << endl;
cout << "Press 10: October" << endl;
cout << "Press 11: November" << endl;
cout << "Press 12: December" << endl;
cout << "Enter Number: "; cin >> date;

switch(date){
case 1:
case 3:
case 5:
case 7:
case 8:
case 10:
case 12:
	cout << "There is 31 Days in the month you've chose" << endl;
	break;
case 4:
case 6:
case 9:
case 11:
	cout << "There is 30 days in the month you've chose" << endl;
	break;
case 2:
	cout << "There is 29 days in the month you've chose" << endl;
	break;
default:
	cout << "INVALID" << endl;
	break;
}

return 0;
}

//Fuel me up #include using namespace std;

int main() {

int fuel;
char type;

cout << "(100 - 0) How much fuel does your vehicle has: "; cin >>fuel;
if (fuel >= 0 && fuel <= 100) {
	cout << "Please choose type of fuel" << endl;
	cout << "Press 'p' for petrol. Press 'd' for diesel: "; cin >> type;
	switch (type) {
	case'd':
	case'D': {
		cout << "You have chose diesel, You need to fuel " << 100 - fuel << " To reach full tank again" << endl;
	}
		break;
	case'p':
	case'P': {
		cout << "You have chose petrol, You need to fuel " << 100 - fuel << " To reach full tank again" << endl;
	}
		break;
	default:
		system("cls");
		cout << "INVALID INPUT" << endl;
		break;
	}

}
else {
	system("cls");
	cout << "INVALID INPUT" << endl;
}

return 0;
}

//Switching Temperature #include #include <ctype.h> #include using namespace std;

int main() {

char type = 0;
double temp = 0;
string strInput;
char szInput[16] = { 0 };

cout << "Press 'f' to convert fahrenheit to celsius. Press 'c' to convert celsius to fahrenheit: "; cin >> type;

switch (type) {
case 'f':
case 'F':
	cout << "You have choose fahrenheit to celsius, Enter the temperature: ";
	cin >> strInput;
	strcpy_s(szInput, strInput.c_str());

	if (isalpha(szInput[0])) {
		system("cls");
		cout << "INVALID" << endl;
	}
	else {
		temp = atof(szInput);
		cout << "in Fahrenheit: " << temp << endl;
		cout << "in Celsius: " << temp - 32 * 0.5556;
	}

	break;
case 'c':
case 'C':

	cout << "You have choose celsius to fahrenheit, Enter the temperature: "; cin >> strInput;
	strcpy_s(szInput, strInput.c_str());
	if (isalpha(szInput[0])) {
		system("cls");
		cout << "INVALID" << endl;

	}
	else {
		temp = atof(szInput);
		cout << "in Celsius: " << temp << endl;
		cout << "in Fahrenheit: " << (temp * 1.8)+32;
	}
	break;
default:
	system("cls");
	cout << "INVALID INPUT" << endl;
	break;
}


return 0;
}

//Switch Grade Calculator #include using namespace std;

int main() {

int grade, result;

cout << "(100 - 0) Enter the grade: "; cin >> grade;
if (cin.fail()) {
	system("cls");
	cout << "INVALID INPUT" << endl;
}else if (grade >= 0 && grade <= 100) {
	result = grade / 10;
	switch (result) {
	default:
		system("cls");
		cout << "INVALID INPUT" << endl;
		break;
	case 0:
	case 1:
	case 2:
	case 3:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: F";
		break;
	case 4:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: E";
		break;
	case 5:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: D";
		break;
	case 6:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: C";
		break;
	case 7:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: B";
		break;
	case 8:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: A";
		break;
	case 9:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: A";
		break;
	case 10:
		cout << "Entered Grade: " << grade;
		cout << "\nMark: A";
		break;
	}
}else {
	system("cls");
	cout << "INVALID INPUT" << endl;
}

return 0;
}
