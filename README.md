Checking if two strings are Anagram or Not
In this article we will learn how to code a C++ program to check if two strings are anagram or not. If two strings have same frequency of  characters and only the order of characters is different then such strings are said to be anagram. So to check if the strings are anagram or not we will take both the string as input then we will count the frequency of characters presents in both string. we will use while loop to count the frequency of characters. Then if  the frequency of both string matches then they are anagram.

Checking if two strings are anagram or not in C
Algorithm:
Initialize the variables and accept the input.
Calculate frequencies of both the strings.
Check ,if frequencies of characters in both the string matches or not.
If frequencies are same set flag =0 , else set flag=1.
If flag= 0, string are anagram else they are not.
Print result.
C++ programming code to check if two strings are anagram or not
#include<iostream> 
using namespace std;
int main()
{
    //Initializing variables.
    char str1[100],str2[100];
    int first[26]={0}, second[26]={0}, c=0, flag=0;
    
    //Accepting inputs.
    cout<<"Enter First String: ";
    gets(str1);
    cout<<"Enter Second String: ";
    gets(str2);
    
    //Calculating frequencies of characters in first string.
    while(str1[c] != '\0')
    {
        first[str1[c]-'a']++;
        c++;
    }
     
    c=0;
    //Calculating frequencies of characters in second string. 
    while(str2[c] != '\0')
    {
        second[str2[c]-'a']++;
        c++;
    }
    //Checking if frequencies of both the strings are same or not.
    for(c=0;c<26;c++)
    {
        if(first[c] != second[c])
            flag=1;
    }
    //Priting result.
    if(flag == 0)
    {
        cout<<"Strings are anagram.";
    }
    else
    {
        cout<<"Strings are not anagram.";
    }
    return 0;
  
}
Enter First String: listen
Enter Second String: silent
Strings are anagram.
