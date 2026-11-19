# Cyber Work
Programming work
Repo Name  `CPP-Programs-BSCBS`

*1. 01_hello_world.cpp*
#include <iostream>
using namespace std;
int main() {
    cout << "Hello World! Welcome to C++" << endl;
    return 0;
}
*2. 02_sum_of_two_numbers.cpp*
#include <iostream>
using namespace std;
int main() {
    int a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    cout << "Sum = " << a + b << endl;
    return 0;
}
*3. 03_even_odd.cpp*
#include <iostream>
using namespace std;
int main() {
    int n;
    cout << "Enter number: ";
    cin >> n;
    if (n % 2 == 0) cout << "Even" << endl;
    else cout << "Odd" << endl;
    return 0;
}
*4. 04_largest_of_three.cpp*
#include <iostream>
using namespace std;
int main() {
    int a, b, c;
    cout << "Enter three numbers: ";
    cin >> a >> b >> c;
    if (a >= b && a >= c) cout << a << " is Largest";
    else if (b >= a && b >= c) cout << b << " is Largest";
    else cout << c << " is Largest";
    return 0;
}
*5. 05_factorial.cpp*
#include <iostream>
using namespace std;
int main() {
    int n, fact = 1;
    cout << "Enter number: ";
    cin >> n;
    for (int i = 1; i <= n; i++) fact *= i;
    cout << "Factorial = " << fact << endl;
    return 0;
}
*6. 06_fibonacci_series.cpp*
#include <iostream>
using namespace std;
int main() {
    int n, a = 0, b = 1, c;
    cout << "Enter terms: ";
    cin >> n;
    for (int i = 0; i < n; i++) {
        cout << a << " ";
        c = a + b; a = b; b = c;
    }
    return 0;
}
*7. 07_prime_number.cpp*
#include <iostream>
using namespace std;
int main() {
    int n, flag = 0;
    cout << "Enter number: ";
    cin >> n;
    for (int i = 2; i <= n/2; i++) if (n % i == 0) flag = 1;
    if (flag == 0 && n > 1) cout << "Prime";
    else cout << "Not Prime";
    return 0;
}
*8. 08_palindrome.cpp*
#include <iostream>
using namespace std;
int main() {
    int n, rev = 0, temp;
    cout << "Enter number: ";
    cin >> n;
    temp = n;
    while (temp > 0) { rev = rev*10 + temp%10; temp /= 10; }
    if (rev == n) cout << "Palindrome";
    else cout << "Not Palindrome";
    return 0;
}
*9. 09_simple_calculator.cpp*
#include <iostream>
using namespace std;
int main() {
    char op; float a, b;
    cout << "Enter operator (+,-,*,/): "; cin >> op;
    cout << "Enter two numbers: "; cin >> a >> b;
    switch(op) {
        case '+': cout << a+b; break;
        case '-': cout << a-b; break;
        case '*': cout << a*b; break;
        case '/': cout << a/b; break;
        default: cout << "Invalid";
    }
    return 0;
}
*10. 10_array_sum_average.cpp*
#include <iostream>
using namespace std;
int main() {
    int arr[5], sum = 0;
    cout << "Enter 5 numbers: ";
    for (int i = 0; i < 5; i++) { cin >> arr[i]; sum += arr[i]; }
    cout << "Sum = " << sum << endl;
    cout << "Average = " << sum / 5.0 << endl;
    return 0;
}
*11. 11_matrix_addition.cpp*
#include <iostream>
using namespace std;
int main() {
    int a[2][2], b[2][2], c[2][2];
    cout << "Enter Matrix A (4 values): ";
    for (int i=0;i<2;i++) for(int j=0;j<2;j++) cin >> a[i][j];
    cout << "Enter Matrix B (4 values): ";
    for (int i=0;i<2;i++) for(int j=0;j<2;j++) cin >> b[i][j];
    for (int i=0;i<2;i++) {
        for(int j=0;j<2;j++) { c[i][j]=a[i][j]+b[i][j]; cout << c[i][j] << " "; }
        cout << endl;
    }
    return 0;
}
*12. 12_reverse_string.cpp*
#include <iostream>
#include <string>
using namespace std;
int main() {
    string s;
    cout << "Enter string: ";
    getline(cin, s);
    for (int i = s.length()-1; i >= 0; i--) cout << s[i];
    return 0;
}
*13. 13_function_max.cpp*
#include <iostream>
using namespace std;
int findMax(int a, int b) {
    return (a > b) ? a : b;
}
int main() {
    int x, y;
    cout << "Enter two numbers: ";
    cin >> x >> y;
    cout << "Max = " << findMax(x, y);
    return 0;
}
*14. 14_class_student.cpp*
#include <iostream>
using namespace std;
class Student {
public:
    string name;
    int roll;
    void display() {
        cout << "Name: " << name << endl;
        cout << "Roll No: " << roll << endl;
    }
};
int main() {
    Student s1;
    s1.name = "Zainab"; s1.roll = 101;
    s1.display();
    return 0;
}
*15. 15_file_handling.cpp*
#include <iostream>
#include <fstream>
using namespace std;
int main() {
    ofstream file("data.txt");
    file << "Hello, This is my C++ File Handling Program.";
    file.close();
    cout << "Data written to file successfully!";
    return 0;
}
---
