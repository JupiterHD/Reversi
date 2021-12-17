#include <iostream>

using namespace std;

class Reversi
{
    public:
        string xcoord = "ABCDEFGH", ycoord = "12345678";
        char board[8][8], player = '2';
        void start()
        {
            for(int i = 1; i < 9; i++)
            {
                for(int j = 1; j < 9; j++)
                {
                    if((i == 4 && j == 4)||(i == 5 && j == 5))
                    {
                        board[i-1][j-1] = '2';
                        continue;
                    }
                    if((i == 4 && j == 5)||(i == 5 && j == 4))
                    {
                        board[i-1][j-1] = '1';
                        continue;
                    }
                    board[i-1][j-1] = '0';
                }
            }
        }

        void checkWin()
        {
            int one = 0, two = 0;
            for(int i = 0; i < 8; i++)
            {
                for(int j = 0; j < 8; j++)
                {
                    if(board[i][j] == '1') one += 1;
                    if(board[i][j] == '2') two += 1;
                }
            }
            if(one > two) cout << "1 ";
            else if(two > one) cout << "2 ";
            else cout << "0 ";
            cout << one << " " << two << endl;
        }

        void setBoard()
        {
            char nboard[8][8];
            for(int i = 0; i < 8; i++)
            {
                string str;
                cin >> str;
                for(int j = 0; j < 8; j++)
                {
                    board[i][j] = str[j];
                }
            }
        }

        void printBoard()
        {
            for(int i = 0; i < 8; i++)
            {
                for(int j = 0; j < 8; j++)
                {
                    cout << board[i][j];
                }
                cout << endl;
            }
        }

        void changePlayer()
        {
            if (player == '2') player = '1';
            else player = '2';
        }

        int numTurns()
        {
            int number = 0;
            for(int i = 0; i < 8; i++)
            {
                for(int j = 0; j < 8; j++)
                {
                    if(board[i][j] == '1' || board[i][j] == '2') number++;
                }
            }
            return number-4;
        }

        void turn(string coords)
        {
            int x, y;
            for(int i = 0; i < 8; i++)
            {
                if (coords[0] == xcoord[i])
                {
                    x = i;
                }

                if (coords[1] == ycoord[i])
                {
                    y = i;
                }
            }
            board[y][x] = player;
            //Нужно дописать превращение чужих фишек в свои
        }
};

int main()
{
    return 0;
}
