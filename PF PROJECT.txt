#include <iostream>
#include <string>
using namespace std;

void StartAdventure()
{
    string choice1, choice2;
    char password[9];
    string correctPassword = "treasure";
    char* passwordPtr = password;

    cout << "You wake up and find yourself stuck in a cave with no memory of how you got in "
         << "or which way is out. There's only one thing you can do; find a way out!\n";

    cout << "You see two paths ahead. Do you choose to go left or right?(l/r)\n";
    cin >> choice1;

    if (choice1 == "l")
    {
        cout << "You go left and immediately fall into a bottomless pit! Aaaaaaaaaaaaaaah! "
             << "GAME OVER!\n";
    }
    else if (choice1 == "r")
    {
        cout << "You go right, and see a shovel and an axe on the ground. Which one do you pick?(s/a)\n";
        cin >> choice2;

        if (choice2 == "s")
        {
            cout << "You take the axe and move forward. You see two paths. Do you go left or right?(l/r)\n";
            cin >> choice1;

            if (choice1 == "l")
            {
                cout << "You encounter a bear and it attacks you. You try to defend yourself using the shovel, "
                     << "but the bear was too fast, and now you're dead! GAME OVER!\n";
            }

            else if (choice1 == "r")
            {
                cout << "As soon as you step foot on the path, bats attack you! GAME OVER!\n";
            }

            else
            {
                cout << "INVALID INPUT! GAME OVER!\n";
            }
        }

        else  if (choice2 == "a")
        {
            cout << "You take the axe and move forward. You see two paths. Do you go left or right?(l/r)\n";
            cin >> choice1;

            if (choice1 == "l")
            {
                cout << "You encounter a bear and it attacks you. You use your axe to defend yourself. "
                     << "The bear is now dead! You proceed to move forward.\n";

                cout << "Now, you see two more paths. There is light coming from one of them, and the "
                     << "other is completely dark. Which one do you choose?(l/d)\n";
                cin >> choice2;

                if (choice2 == "l")
                {
                    cout << "You move towards the light, hoping that it will show you the way out, but "
                         << "it turns out to be lava. You are shocked but try not to worry because there is "
                         << "an old wooden bridge. You step one foot onto the bridge and it immediately collapses "
                         << "because it couldn't support your weight. GAME OVER!\n";
                }

                else if (choice2 == "d")
                {
                    cout << "You move towards the dark path. You see two ladders, one leads downwards "
                         << "and the other upwards. Which way do you go?(u/d)\n";
                    cin >> choice1;

                    if (choice1 == "d")
                    {
                        cout << "You go down and  see something in the dark. You move closer and see that "
                             << "it's a statue. As soon as you touch it, you are turned to stone. GAME OVER!\n";
                    }

                    else  if (choice1 == "u")
                    {
                        cout << "You go up and see two more paths. Do you go left or right?(l/r)\n";
                        cin >> choice2;

                        if (choice2 == "l")
                        {
                            cout << "You go to the left path and see a lamp. Do you wish to rub it?(y/n)\n";
                            cin >> choice1;

                            if (choice1 == "y")
                            {
                                cout << "You rub the lamp, hoping that a genie will come out and grant you "
                                     << "three wishes. It's a trap. The genie comes out and traps you in "
                                     << "the lamp instead! GAME OVER!\n";
                            }

                            else  if (choice1 == "n")
                            {
                                cout << "You decide not to rub the lamp and move forward. You enter a "
                                     << "smaller cave and encounter a zombie. It attacks you and you aren't "
                                     << "able to defend yourself. You are now a zombie! GAME OVER!\n";
                            }
                        }

                        else if (choice2 == "r")
                        {
                            cout << "You go to the right path and accidentally trip over a rock. You hit your "
                                 << "head on the ground and your head starts bleeding. You feel dizzy, but "
                                 << "you still gather some strength and decide to continue on.\n";

                            cout << "After a while, you see two smaller caves. Which one do you choose?(l/r)\n";
                            cin >> choice1;

                            if (choice1 == "l")
                            {
                                cout << "You find a locked chest. You need a password to open it. "
                                     << "You look around for clues and find some jumbled-up letters "
                                     << "written on the wall: saetreur. Unscramble the letters and enter the password.\n";

                                for (int i = 0; i < 8; i++)
                                {
                                    cout << "Enter letter " << i + 1 << ": ";
                                    cin >> *(passwordPtr + i);
                                }
                                *(passwordPtr + 8) = '\0';

                                if (string(passwordPtr) == correctPassword)
                                {
                                    cout << "CONGRATULATIONS! You have unlocked the chest. "
                                         << "There are two potions inside. One is red and the other "
                                         << "is green. Which one do you choose?(r/g)\n";
                                    cin >> choice2;

                                    if (choice2 == "g")
                                    {
                                        cout << "You drink the green potion. Oh No! You are now a frog. "
                                             << "GAME OVER!\n";
                                    }

                                    else if (choice2 == "r")
                                    {
                                        cout << "You drink the red potion. Yay! You now have super "
                                             << "strength. You move further into the cave.\n";

                                        cout << "After a tiring, long walk you see two paths. One is being "
                                             << "blocked by a boulder, and the other is unblocked. "
                                             << "Which one do you choose?(b/u)\n";
                                        cin >> choice1;

                                        if (choice1 == "u")
                                        {
                                            cout << "You choose the unblocked path and meet a wizard. He "
                                                 << "offers his help. Do you take it?(y/n)\n";
                                            cin >> choice2;

                                            if (choice2 == "y")
                                            {
                                                cout << "You choose to take his help, but Oh No! it's a "
                                                     << "trap! He turns you into a mouse. GAME OVER!\n";
                                            }

                                            else if (choice2 == "n")
                                            {
                                                cout << "You choose not to take his help and move forward. "
                                                     << "You stop somewhere and suddenly a huge stone slab falls and "
                                                     << "crushes you. GAME OVER!\n";
                                            }

                                            else
                                            {
                                                cout << "INVALID INPUT! GAME OVER!\n";
                                            }
                                        }

                                        else if (choice1 == "b")
                                        {
                                            cout << "You use your super strength to move the boulder and "
                                                 << "it turns out that the boulder was blocking the exit! "
                                                 << "\nCONGRATULATIONS! YOU WIN!\n";
                                        }

                                        else
                                        {
                                            cout << "INVALID INPUT! GAME OVER!\n";
                                        }
                                    }

                                    else
                                    {
                                        cout << "INVALID INPUT! GAME OVER!\n";
                                    }
                                }

                                else
                                {
                                    cout << "INVALID PASSWORD! The chest explodes! GAME OVER!\n";
                                }
                            }

                            else
                            {
                                cout << "INVALID INPUT! GAME OVER!\n";
                            }
                        }

                        else
                        {
                            cout << "INVALID INPUT! GAME OVER!\n";
                        }
                    }

                     else
                     {
                         cout << "INVALID INPUT! GAME OVER!\n";
                     }
                }

                 else
                 {
                     cout << "INVALID INPUT! GAME OVER!\n";
                 }
            }

            else if (choice1 == "r")
            {
                cout << "As soon as you step foot on the path, it immediately caves in, and "
                     << "you fall to your death! GAME OVER!\n";
            }

            else
            {
                cout << "INVALID INPUT! GAME OVER!\n";
            }
        }

         else
         {
             cout << "INVALID INPUT! GAME OVER!\n";
         }
    }

    else
    {
        cout << "INVALID INPUT! GAME OVER!\n";
    }
}

int main()
{
    char PlayAgain;
    do
    {
        cout << "Welcome to LOST IN THE CRYPTIC CAVERNS!\n";
        cout << "\"NOTE: USE LOWERCASE LETTERS OR YOU'LL HAVE TO START OVER!\"\n\n";

        StartAdventure();

        cout << "Do you want to play again?(y/n)\n";
        cin >> PlayAgain;
        cout << endl;

    } while (PlayAgain == 'y');

    cout << "Thank you for playing the game!\n";
    cout << "GOODBYE!\n";

    return 0;
}