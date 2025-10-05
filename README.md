# 🧩 C++ Utility Library — clsPrint & clsInputValidate

A modern and reusable **C++ helper library** for efficient console output and robust input validation.  
It provides two key classes:

- 🖨️ clsPrint — for printing and formatting data beautifully in the console.  
- ✅ clsInputValidate — for validating user input of any type safely and interactively.

---

## ✨ Overview

🔹 clsPrint:  
Enables clean, readable, and feature-rich console printing — from text formatting and random data generation to mathematical pattern output.

🔹 clsInputValidate:  
Handles user input safely, checking for type errors, number ranges, positivity, odd/even/prime/perfect/palindrome properties, and more.

---
## 📁 Project Structure
### ✨ CppUtilityLibrary

📜 clsPrint.h — Printing and formatting class

📜 clsInputValidate.h — Input validation class

📜 clsString.h — String helper utilities (vowels, parsing, etc.)

📜 clsMath.h — Math helper utilities (prime, palindrome, perfect, etc.)

📜 clsUtil.h — Utility helper (random chars, keys, levels)

📜 main.cpp — Example usage and testing

📄 README.md — Documentation file

---

## 🧾 Features

### 🖨️ clsPrint
| Category | Description |
|-----------|--------------|
| Text | Print text, tabs, vowels, first letters, and words |
| Numbers | Print digits, Fibonacci, even/odd/prime/palindrome/perfect numbers |
| Random | Generate random uppercase, lowercase, and special characters |
| Math Integration | Uses clsMath for prime, palindrome, and perfect checks |
| Files | Save strings to text files easily |
| Console Effects | Change screen colors, alerts, and game result screens |
| Dates | Print short day/month names and formatted week headers |

### ✅ clsInputValidate
| Category | Description |
|-----------|--------------|
| Type Validation | Check if last input was valid |
| Range Checking | Ensure number lies between two values |
| Positive/Negative | Read only positive or negative numbers |
| Odd/Even | Read numbers constrained by parity |
| Prime/Perfect/Palindrome | Validate based on mathematical properties |
| Characters & Strings | Read single characters and full strings |
| Arrays | Read arrays of numbers, strings, or characters |
| Enum Input | Read operation types and difficulty levels safely |

---

## ⚙️ Example Usage (main.cpp)

#include <iostream>
#include "clsPrint.h"
#include "clsInputValidate.h"
using namespace std;

int main()
{
    clsPrint::Print("Hello from clsPrint!\n");
    cout << clsPrint::Tabs(2) << "Indented text example\n";

    cout << "Prime numbers from 1 to 20: ";
    clsPrint::PrintPrimeNumbers(1, 20);

    cout << "Perfect numbers from 1 to 500: ";
    clsPrint::PrintPerfectNumbers(1, 500);

    cout << "\nRandom upper letters: ";
    clsPrint::PrintRandomUpperLetters(5);
    cout << endl;

    clsPrint::PrintFirstLetterOfWords("Hello World From clsPrint");
    clsPrint::PrintVowels("Programming is Fun!");
    clsPrint::SaveStringToFile("output.txt", "Saved line example.");

    cout << "\nEnter a number between 1 and 10: ";
    int num = clsInputValidate::ReadNumberBetween<int>(1, 10);
    cout << "✅ You entered: " << num << endl;

    cout << "Enter a positive number: ";
    int pos = clsInputValidate::ReadPositiveNumber<int>();
    cout << "✅ Positive number accepted: " << pos << endl;

    cout << "Enter a prime number: ";
    int prime = clsInputValidate::ReadPrimeNumber<int>();
    cout << "✅ Prime number accepted: " << prime << endl;

    return 0;
}

---

## 🧪 Sample Output

Hello from clsPrint!
        Indented text example
Prime numbers from 1 to 20: 2 3 5 7 11 13 17 19
Perfect numbers from 1 to 500: 6 28 496
Random upper letters: QWTRB

 First Letter of this string 
H
W
F
C

 Vowels In String are : o a i i u

Enter a number between 1 and 10: 7
✅ You entered: 7
Enter a positive number: 15
✅ Positive number accepted: 15
Enter a prime number: 13
✅ Prime number accepted: 13

---

## 🧠 Class Reference

🖨️ clsPrint — Public Methods
--------------------------------

static void Print(string text);                         // Print a string to the console
static string Tabs(int count);                          // Return tab spacing for indentation
static void PrintPrimeNumbers(int from, int to);        // Print all prime numbers in a range
static void PrintEvenNumbers(int from, int to);         // Print even numbers in a range
static void PrintOddNumbers(int from, int to);          // Print odd numbers in a range
static void PrintPerfectNumbers(int from, int to);      // Print perfect numbers in a range
static void PrintPalindromeNums(int from, int to);      // Print palindrome numbers in a range
static void PrintFibonatchiSerie(int number);           // Print a Fibonacci sequence
static void PrintFirstLetterOfWords(string s);          // Print the first letter of each word
static void PrintVowels(string s);                      // Print all vowels in a string
static void PrintEachWord(string s);                    // Print each word on a new line
static void SaveStringToFile(string filename, string text); // Save text to a file


clsInputValidate
--------------------------------
static bool IsValidLastInput();
template<typename T> static bool IsNumberBetween(T number, T from, T to);
template<typename T> static T ReadNumber(string errorMsg);
template<typename T> static T ReadNumberBetween(T from, T to, string errorMsg);
template<typename T> static T ReadPositiveNumber(string errorMsg);
template<typename T> static T ReadNegativeNumber(string errorMsg);
template<typename T> static T ReadOddNumber(string errorMsg);
template<typename T> static T ReadEvenNumber(string errorMsg);
template<typename T> static T ReadPrimeNumber(string errorMsg);
template<typename T> static T ReadPerfectNumber(string errorMsg);
template<typename T> static T ReadPalindromeNumber(string errorMsg);
static string ReadString();
static char ReadCharacter(string errorMsg);
static bool ReadBoolean(string errorMsg);

---

## 💡 Example Use Cases

- Interactive console programs  
- Educational exercises (math, validation, string parsing)  
- Small games or quizzes  
- Command-line utilities  
- Training projects for C++ OOP practice  

---

## 🧰 Requirements

- C++17 or newer  
- Standard I/O stream libraries (<iostream>, <string>, <limits>, <fstream>)  
- Include all helper headers (clsMath, clsString, clsUtil) in your project folder  

---

## 👨‍💻 Author

Developed by: [Faresincode]  
💬 Contributions, issues, and improvements are welcome!

---

## 🪪 License

This project is open-source under the MIT License — free to use, modify, and share.
