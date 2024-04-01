[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Fmb6W2KK)
Design a C++ program for an employee payroll system. Create classes for Employee and Payroll. Users can add employees, enter hours worked, calculate salaries, and generate payroll reports.
#include <iostream>
#include <string>
using namespace std;
struct Book 
{
    string isbn;
    string title;
    string author;
    int year;
    string genre;
};

void searchBook(const Book library[], int size, const string& isbn) 
{

    bool found = false;
    for (int i = 0; i < size; ++i) 
	{
        if (library[i].isbn == isbn) 
		{
            found = true;
            cout << "Book found!" << endl;
            cout << "Title: " << library[i].title << endl;
            cout << "Author: " << library[i].author << endl;
            cout << "Year: " << library[i].year << endl;
            cout << "Genre: " << library[i].genre << endl;
            break;
        }
    }
    
    if (!found) 
	{
        cout << "Book not available in the library." << endl;
    }
}

int main() 
{
	cout<<"TANVEER KAUR\n";
	cout<<"2310997301\n";
	const int librarySize = 4;
    Book library[librarySize] = 
	{
        {"978-1400079172", "The Catcher in the Rye", "J.D. Salinger", 1951, "Fiction"},
        {"978-0141182551", "1984", "George Orwell", 1949, "Science Fiction"},
        {"978-0061120084", "To Kill a Mockingbird", "Harper Lee", 1960, "Fiction"},
        {"978-1451673319", "The Great Gatsby", "F. Scott Fitzgerald", 1925, "Fiction"}
    };

    cout << "Enter the ISBN of the book you want to search for: ";
    string isbn;
    cin >> isbn;

    searchBook(library, librarySize, isbn);

    return 0;
}
