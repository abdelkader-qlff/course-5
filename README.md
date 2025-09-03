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
