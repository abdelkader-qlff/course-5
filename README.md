problem #1:
#include <iostream>
using namespace std;
void width() {
	cout << "\t\t\t\tMultiple Table from 1 to 10\n\n";
	for (int i = 1; i <= 10; i++) {
		cout << "\t" << i;
	}
	cout << "\n-----------------------------------------------------------------------------------\n";
}
string separatorligne(int i) {
	if (i < 10)
		return "   |";
	else
		return "  |";
}
void lenght() {
	width();
	for (int i = 1; i <= 10; i++) {
		cout << i << separatorligne(i) << "\t";
		for (int x = 1; x <= 10; x++) {
			cout << x * i << "\t";
		}
		cout << endl;
	}
}
int main() {
	lenght();
}

problem #2:
#include <iostream>
#include <string>
using namespace std;
enum enprimenotprime { Prime = 1, Notprime = 2 };
int readnumber(string message) {
	int number = 0;
	do {
		cout << message << endl;
		cin >> number;
	} while (number <= 0);
	return number;
}
enprimenotprime choosegenre(int num) {
	if (num < 2)
		return Notprime;
	for (int i = 2; i <= num / 2; i++) {
		if (num % i == 0)
			return Notprime;
	}
	return Prime;
}
void printprimenums() {
	int N = readnumber("enter a positive number: ");
	cout << "Prime number:\n";
	for (int i = 1; i <= N; i++) {
		if (choosegenre(i) == Prime)
			cout << "\t" << i ;
	}
}
int main() {
	printprimenums();
}

problem #3:
