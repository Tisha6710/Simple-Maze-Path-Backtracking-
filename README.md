# Simple-Maze-Path-Backtracking-
package BackTracking;

public class MazePath {
    public static void main(String[] args) {
        int rows=3;
        int col=3;
        int count= maze(1,1,rows,col);
        System.out.println(count);


    }
// sr-starting row,sc=starting column,er=ending row,ec=ending column
    private static int maze(int sr, int sc, int er, int ec){
        if(sr>er || sc>ec) return 0;
        if(sr==er && sc==ec) return 1;
        int downWays=maze(sr+1,sc,er,ec); // niche jayenge toh rows incresse
        int rightWays=maze(sr,sc+1,er,ec);
int totalways=downWays+rightWays;
return totalways;
    }
}
