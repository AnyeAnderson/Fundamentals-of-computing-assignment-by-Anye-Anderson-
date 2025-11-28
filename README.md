# Fundamentals-of-computing-assignment-by-Anye-Anderson-
Fundamentals of Computing Assignment solution by Anye Anderson 

#include <iostream>
#include <cmath>
#include <complex>

Function to solve a quadratic equation
void solveQuadratic(double a, double b, double c) {
    Calculate the discriminant
    double d = b*b - 4*a*c;

    If d is positive, the equation has two real roots
    if (d > 0) {
        double root1 = (-b + sqrt(d)) / (2*a);
        double root2 = (-b - sqrt(d)) / (2*a);
        std:cout << "The roots of the equation are: " << root1 << " and " << root2 << std:endl;
    }

    If d is zero, the equation has one real root
    else if (d == 0) {
        double root = -b / (2*a);
        std:cout << "The equation has one real root: " << root << std:endl;
    }

    If d is negative, the equation has two complex roots
    else {
        std:complex<double> root1 = (-b + std:complex<double>(0, sqrt(-d))) / (2*a);
        std:complex<double> root2 = (-b - std:complex<double>(0, sqrt(-d))) / (2*a);
        std:cout << "The roots of the equation are: " << root1 << " and " << root2 << std:endl;
    }
}

int main() {
    double a, b, c;

    Input coefficients
    std:cout << "Enter the coefficient of x^2: ";
    std:cin >> a;
    std:cout << "Enter the coefficient of x: ";
    std:cin >> b;
    std:cout << "Enter the constant term: ";
    std:cin >> c;

    Solve the equation
    solveQuadratic(a, b, c);

    return 0;
}
