public class Board {

    static final int WIDTH = 19;
    static final int HEIGHT = 19;
    int[][] board = new int[HEIGHT][WIDTH];


    //Board Contructor
    public Board() {
        for (int i = 0; i < HEIGHT; i++) {
            for (int j = 0; j < WIDTH; j++) {
                board[i][j] = 0;
            }
        }
    }

    //Places token for player
    public boolean place(int row, int column, int player) {
            if (board[row][column] == 0) {
                board[row][column] = player;
            }
            return this.hasWin(row, column, player);
    }

    //Checks to see if the player won the game horizontally
    public boolean hasHorizontalWin(int row, int column,int player) {
        int total = 1;
        //Counts connections made on left side of placement
        for ( int k = row - 1; k >= 0 && k > row - 5; --k ) {
            if ( board[k][column] != player ) break;
            ++total;
        }
        for ( int k = row + 1; k < HEIGHT && k < row + 5; ++k ) {
            if ( board[k][column] != player ) break;
            ++total;
        }
        return total >= 5;
    }

    //Checks to see if the player won the game vertically
    public boolean hasVerticalWin(int row, int column, int player) {
        int total = 1;
        //Counts connections made on left side of placement
        for ( int k = column - 1; k >= 0 && k > column - 5; --k ) {
            if ( board[row][k] != player ) break;
            ++total;
        }
        for ( int k = column + 1; k < WIDTH && k < column + 5; ++k ) {
            if ( board[row][k] != player ) break;
            ++total;
        }
        return total >= 5;
    }
    //Player wins method
    boolean hasWin(int row, int column, int player) {
        if (this.hasHorizontalWin(row, column, player) == true ||
            this.hasVerticalWin(row, column, player) == true) {
                System.out.println("Player " + player + " wins!");
                return true;
        } else return false;
    }

    //Prints board as string
    public void printBoard(){
        for (int m = 0; m < HEIGHT; m++){
            for (int b = 0 ; b < WIDTH; b++){
                if (board[m][b] == 0) System.out.print("-");
                if (board[m][b] == 1) System.out.print("o");
                if (board[m][b] == 2) System.out.print("x");
            }
            System.out.println();
        }
    }
}
