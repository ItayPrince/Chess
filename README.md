# Chess
Knight Rook and Bishop threats



import java.util.Scanner;
public class Chess
{
    public static void main (String [] args){
        
        int count = 0;

        Scanner scan = new Scanner (System.in);
        System.out.println("Please enter the type"+
            " of the first chessman");
        char first = scan.next().charAt(0);
        System.out.println ("Please enter the number of row");
        int row1 = scan.nextInt();
        System.out.println ("Please enter the number of column");
        int col1 = scan.nextInt();
        System.out.println("Please enter the type"+
            " of the second chessman");
        char second = scan.next().charAt(0);
        System.out.println ("Please enter the number of row");
        int row2 = scan.nextInt();
        System.out.println ("Please enter the number of column");
        int col2 = scan.nextInt();
        
        String tempSecond;
        if(second == 'r')
            tempSecond = "Rook";
            else if (second == 'k')
            tempSecond = "Knight";
            else 
            tempSecond = "Bishop";
            
        
        if(first == second)
            System.out.println("Chessmen should be different from each other");
            else if (row1 == row2 && col1 == col2)
                System.out.println("Chessmen positions should not be identical");
            else if ((row1 > 8 || row2 > 8 || col1 > 8 || col2 > 8) 
                        || (row1 < 1 || row2 < 1 || col1 < 1 || col2 < 1 ))
                System.out.println("Position is not legal");
            else switch(first){
                
                
            case 'r': // Checking Rook threats on second chessman
                int tempRow = row1; /* each block move to possiable location and
                                     check for threats */
                --tempRow; // row-
                if((tempRow == row2 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat1 " + tempSecond);
                --tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat2 " + tempSecond);
                --tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat3 " + tempSecond);
                --tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat4 " + tempSecond);
                --tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat5 " + tempSecond);
                --tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat6 " + tempSecond);
                --tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat7 " + tempSecond);
                
                count++; // counting no threats
                
                tempRow = row1;
                ++tempRow; // row+
                if((tempRow == row2 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat8 " + tempSecond);
                ++tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat9 " + tempSecond);
                ++tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat10 " + tempSecond);
                ++tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat11 " + tempSecond);
                ++tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat12 " + tempSecond);
                ++tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat13 " + tempSecond);
                ++tempRow;
                if((tempRow == row2 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat14 " + tempSecond);
                
                int tempCol = col1;
                ++tempCol; // col+
                if((row1 == row2 && tempCol == col2) && tempCol < 9)
                System.out.println("Rook threat15 " + tempSecond);
                ++tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol < 9)
                System.out.println("Rook threat16 " + tempSecond);
                ++tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol < 9)
                System.out.println("Rook threat17 " + tempSecond);
                ++tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol < 9)
                System.out.println("Rook threat18 " + tempSecond);
                ++tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol < 9)
                System.out.println("Rook threat19 " + tempSecond);
                ++tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol < 9)
                System.out.println("Rook threat20 " + tempSecond);
                ++tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol < 9)
                System.out.println("Rook threat21 " + tempSecond);
                ++tempCol;
                
                tempCol = col1;
                --tempCol; // col-
                if((row1 == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Rook threat22 " + tempSecond);
                --tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Rook threat23 " + tempSecond);
                --tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Rook threat24 " + tempSecond);
                --tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Rook threat25 " + tempSecond);
                --tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Rook threat26 " + tempSecond);
                --tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Rook threat27 " + tempSecond);
                --tempCol;
                if((row1 == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Rook threat28 " + tempSecond);
                break;
                
            case 'k': // Knight moves and threat check 
                tempRow = row1-2;
                tempCol = col1+1;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat1 " + tempSecond);
                tempRow = row1-2;
                tempCol = col1-1;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat2 " + tempSecond);
                tempRow = row1+1;
                tempCol = col1-2;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat3 " + tempSecond);
                tempRow = row1-1;
                tempCol = col1-2;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat4 " + tempSecond);
                tempRow = row1+2;
                tempCol = col1-1;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat5 " + tempSecond);
                tempRow = row1+2;
                tempCol = col1+1;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat6 " + tempSecond);
                tempRow = row1+1;
                tempCol = col1+2;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat7 " + tempSecond);
                tempRow = row1-1;
                tempCol = col1+2;
                if(tempRow == row2 && tempCol == col2)
                System.out.println("Knight threat8 " + tempSecond);
                break;
                
            case 'b': // Bishop moves and threat checks
                tempRow = row1; // row- & col-
                tempCol = col1;
                --tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat1 " + tempSecond);
                --tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat2 " + tempSecond);
                --tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat3 " + tempSecond);
                --tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat4 " + tempSecond);
                --tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat5 " + tempSecond);
                --tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat6 " + tempSecond);
                --tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat7 " + tempSecond);
                
                tempRow = row1; // row+ & col-
                tempCol = col1;
                ++tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat8 " + tempSecond);
                ++tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat9 " + tempSecond);
                ++tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat10 " + tempSecond);
                ++tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat11 " + tempSecond);
                ++tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat12 " + tempSecond);
                ++tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat13 " + tempSecond);
                ++tempRow;
                --tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat14 " + tempSecond);
                
                tempRow = row1; // row+ & col+
                tempCol = col1;
                ++tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat15 " + tempSecond);
                ++tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat16 " + tempSecond);
                ++tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat17 " + tempSecond);
                ++tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat18 " + tempSecond);
                ++tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat19 " + tempSecond);
                ++tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat20 " + tempSecond);
                ++tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat21 " + tempSecond);
                
                tempRow = row1; // row- & col+
                tempCol = col1;
                --tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat22 " + tempSecond);
                --tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat23 " + tempSecond);
                --tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat24 " + tempSecond);
                --tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat25 " + tempSecond);
                --tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat26 " + tempSecond);
                --tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat27 " + tempSecond);
                --tempRow;
                ++tempCol;
                if((tempRow == row2 && tempCol == col2) && tempCol > 0)
                System.out.println("Bishop threat28 " + tempSecond);
                break;
            }//end of first switch
                
                
                
                // from now on ,checking if the second chessman threat the first.
                String tempFirst;
        if(first == 'r')
            tempFirst = "Rook";
            else if (first == 'k')
            tempFirst = "Knight";
            else 
            tempFirst = "Bishop";
                
        switch(second){
            case 'r': // Checking Rook threats on second chessman
                int tempRow = row2; /* each block move to possiable location and
                                     check for threats */
                --tempRow; // row-
                if((tempRow == row1 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat1 " + tempFirst);
                --tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat2 " + tempFirst);
                --tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat3 " + tempFirst);
                --tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat4 " + tempFirst);
                --tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat5 " + tempFirst);
                --tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat6 " + tempFirst);
                --tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow > 0)
                System.out.println("Rook threat7 " + tempFirst);
                
                tempRow = row2;
                ++tempRow; // row+
                if((tempRow == row1 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat8 " + tempFirst);
                ++tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat9 " + tempFirst);
                ++tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat10 " + tempFirst);
                ++tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat11 " + tempFirst);
                ++tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat12 " + tempFirst);
                ++tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat13 " + tempFirst);
                ++tempRow;
                if((tempRow == row1 && col1 == col2) && tempRow < 9)
                System.out.println("Rook threat14 " + tempFirst);
                
                int tempCol = col2;
                ++tempCol; // col+
                if((row1 == row2 && tempCol == col1) && tempCol < 9)
                System.out.println("Rook threat15 " + tempFirst);
                ++tempCol;
                if((row1 == row2 && tempCol == col1) && tempCol < 9)
                System.out.println("Rook threat16 " + tempFirst);
                ++tempCol;
                if((row1 == row2 && tempCol == col1) && tempCol < 9)
                System.out.println("Rook threat17 " + tempFirst);
                ++tempCol;
                if((row1 == row2 && tempCol == col1) && tempCol < 9)
                System.out.println("Rook threat18 " + tempFirst);
                ++tempCol;
                if((row1 == row2 && tempCol == col1) && tempCol < 9)
                System.out.println("Rook threat19 " + tempFirst);
                ++tempCol;
                if((row1 == row2 && tempCol == col1) && tempCol < 9)
                System.out.println("Rook threat20 " + tempFirst);
                ++tempCol;
                if((row1 == row2 && tempCol == col1) && tempCol < 9)
                System.out.println("Rook threat21 " + tempFirst);
                ++tempCol;
                
                tempCol = col2;
                --tempCol; // col-
                if((row2 == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Rook threat22 " + tempFirst);
                --tempCol;
                if((row2 == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Rook threat23 " + tempFirst);
                --tempCol;
                if((row2 == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Rook threat24 " + tempFirst);
                --tempCol;
                if((row2 == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Rook threat25 " + tempFirst);
                --tempCol;
                if((row2 == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Rook threat26 " + tempFirst);
                --tempCol;
                if((row2 == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Rook threat27 " + tempFirst);
                --tempCol;
                if((row2 == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Rook threat28 " + tempFirst);
                break;
                
            case 'k': // Knight moves and threat check 
                tempRow = row2-2;
                tempCol = col2+1;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat1 " + tempFirst);
                tempRow = row2-2;
                tempCol = col2-1;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat2 " + tempFirst);
                tempRow = row2+1;
                tempCol = col2-2;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat3 " + tempFirst);
                tempRow = row2-1;
                tempCol = col2-2;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat4 " + tempFirst);
                tempRow = row2+2;
                tempCol = col2-1;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat5 " + tempFirst);
                tempRow = row2+2;
                tempCol = col2+1;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat6 " + tempFirst);
                tempRow = row2+1;
                tempCol = col2+2;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat7 " + tempFirst);
                tempRow = row2-1;
                tempCol = col2+2;
                if(tempRow == row1 && tempCol == col1)
                System.out.println("Knight threat8 " + tempFirst);
                break;
                
            case 'b': // Bishop moves and threat checks
                tempRow = row2; // row- & col-
                tempCol = col2;
                --tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat1 " + tempFirst);
                --tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat2 " + tempFirst);
                --tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat3 " + tempFirst);
                --tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat4 " + tempFirst);
                --tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat5 " + tempFirst);
                --tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat6 " + tempFirst);
                --tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat7 " + tempFirst);
                
                tempRow = row2; // row+ & col-
                tempCol = col2;
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat8 " + tempFirst);
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat9 " + tempFirst);
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat10 " + tempFirst);
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat11 " + tempFirst);
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat12 " + tempFirst);
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat13 " + tempFirst);
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat14 " + tempFirst);
                
                tempRow = row2; // row+ & col+
                tempCol = col2;
                ++tempRow;
                --tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat15 " + tempFirst);
                ++tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat16 " + tempFirst);
                ++tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat17 " + tempFirst);
                ++tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat18 " + tempFirst);
                ++tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat19 " + tempFirst);
                ++tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat20 " + tempFirst);
                ++tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat21 " + tempFirst);
                
                tempRow = row2; // row- & col+
                tempCol = col2;
                --tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat22 " + tempFirst);
                --tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat23 " + tempFirst);
                --tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat24 " + tempFirst);
                --tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat25 " + tempFirst);
                --tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat26 " + tempFirst);
                --tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat27 " + tempFirst);
                --tempRow;
                ++tempCol;
                if((tempRow == row1 && tempCol == col1) && tempCol > 0)
                System.out.println("Bishop threat28 " + tempFirst);
                else count++;
                
                break; 
                
            } //end of second switch
            
             if (count > 0)System.out.println("No Threats");//if we get here , no theats accured
            
    } // end of method main
} //end of class Chess 
