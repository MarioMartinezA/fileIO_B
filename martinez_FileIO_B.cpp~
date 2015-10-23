// Name: Mario Martinez
// Date: 10/22/15
// Description: The program reads in a file containing user grades. It also computes the average of all the students in the list. Also it names the person with the highest average score.

#include <iostream>
#include <fstream>
#include <cstdlib>
#include <string>
#include <iomanip>

using namespace std;

int main()
{
    ifstream in_stream;
    ofstream out_stream;
    
    string firstName, lastName, highScore;
    double score1, score2, score3, score4, score5, score6, average, max = 0;
    
    char fileName[12];
    
    cout << "Enter file name: " << endl;
    cin >> fileName;
    
    in_stream.open(fileName);
    out_stream.open("results.txt");
    
    if(in_stream.fail())
    {
        cout << "Input file opening fail." << endl;
        exit(1);
    }
    
    if(out_stream.fail())
    {
        cout << "Output file opening fail." << endl;
        exit(1);
    }
    
    while(in_stream >> firstName >> lastName >> score1 >> score2 >> score3 >> score4 >> score5 >> score6) //Reading in the file.
    {
    out_stream.setf(ios::fixed); // showing 2 numbers to the right of the decimal
    out_stream.setf(ios::showpoint);
    out_stream.precision(2);
    out_stream.setf(ios::left); // setting up the spacing between each variable.
        average = score1 + score2 + score3 + score4 + score5 + score6;
        average /= 6;
        
        if(max <= average)
        {
            max = average;
            highScore = firstName + " " + lastName;
        }
        //Displaying the names and result as well as their average score. It aslo shows who has the highest score.
        out_stream << setw(10) << firstName << setw(12) << lastName << setw(8) << score1 << setw(8) << score2 << setw(8)
             << score3 << setw(8) << score4 << setw(8) << score5 << setw(8) << score6 << setw(8) << average << endl;
    }
    
    out_stream << "\nHighest score: " << highScore << endl;
    
    in_stream.close();
    out_stream.close();
    
    return 0;
}
