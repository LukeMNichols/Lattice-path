# Lattice-path
C++ code that determines the number of paths between the origin and a point using north-east paths 

#include <iostream>
#include <cmath>
#include <vector>
#include <random>

using namespace std;


int main() {
	int x;
	int y;
	cout << "What is x coordinate?" << "\n";
	cin >> x;
	cout << "What is y coordinate?" << "\n";
	cin >> y;
	int sum = x + y;
	int i;
	int factx = 1;
	int facty = 1;
	int factsum = 1;
	for (i = 1; i <= x; i++) {
		factx *= i;
	}
	for (i = 1; i <= y; i++) {
		facty *= i;
	}
	for (i = 1; i <= sum; i++) {
		factsum *= i;
	}
	int ans = (factsum) / (factx * facty);
	cout << ans << "\n";
	return 0;
}
