# NumberGuessingGame
This is a simple Number Guessing program using cpp programming language.

#include<iostream>
using namespace std;
bool GuessAnswer(int Answer){
 int Number;
 int chances=3;
 int count=0;
 bool gameover=false;
 while(Number!=Answer && !gameover){
    if(count<chances){
    cout<<"Enter Your Number:";
    cin>>Number;
    if(Number==Answer) cout<<"Yey! Correct Guess"<<endl;
    else if(Number==Answer-1 || Number==Answer-2|| Number==Answer+1|| Number==Answer+2)
    cout<<"Your guess is to low."<<endl;
    else
    cout<<"Your guess is to high."<<endl;
    count++;
    }
    else gameover=true;
  }
  if(gameover)cout<<"You Lost!"<<endl<<"Try Again.";
  else cout<<"You Win.";
 
}

int main(){
cout<<"Enter numbers between 0 and 9:"<<endl;;
GuessAnswer(5);
return 0;
}
