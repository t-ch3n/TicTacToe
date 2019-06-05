import java.util.*;
public class TicTacToe{

private static Scanner scan = new Scanner(System.in);
private static String input, input2, pos1, pos2, p1Switch, p2Switch;
public static String[][]arr;

public TicTacToe(){
    
    arr = new String[5][5];
    
        arr[0][0] = " 1 ";
        arr[0][1] = "|";
        arr[0][2] = " 2 ";
        arr[0][3] = "|";
        arr[0][4] = " 3 ";
        arr[1][0] = " - ";
        arr[1][1] = "- ";
        arr[1][2] = "- ";
        arr[1][3] = "- ";
        arr[1][4] = "- ";
        arr[2][0] = " 4 ";
        arr[2][1] = "|";
        arr[2][2] = " 5 ";
        arr[2][3] = "|";
        arr[2][4] = " 6 ";
        arr[3][0] = " - ";
        arr[3][1] = "- ";
        arr[3][2] = "- ";
        arr[3][3] = "- ";
        arr[3][4] = "- ";
        arr[4][0] = " 7 ";
        arr[4][1] = "|";
        arr[4][2] = " 8 ";
        arr[4][3] = "|";
        arr[4][4] = " 9 ";
}

public static void printNewBoard(){
         
        String[][] arr = new String[5][5];
        
        arr[0][0]= " 1 ";
        arr[0][1]="|";
        arr[0][2]=" 2 ";
        arr[0][3]="|";
        arr[0][4]=" 3 ";
        arr[1][0]=" - ";
        arr[1][1]="- ";
        arr[1][2]="- ";
        arr[1][3]="- ";
        arr[1][4]="- ";
        arr[2][0]=" 4 ";
        arr[2][1]="|";
        arr[2][2]=" 5 ";
        arr[2][3]="|";
        arr[2][4]=" 6 ";
        arr[3][0]=" - ";
        arr[3][1]="- ";
        arr[3][2]="- ";
        arr[3][3]="- ";
        arr[3][4]="- ";
        arr[4][0]=" 7 ";
        arr[4][1]="|";
        arr[4][2]=" 8 ";
        arr[4][3]="|";
        arr[4][4]=" 9 ";
        
        
        System.out.println("Welcome to Tic Tac Toe. This is your game board: ");
        TicTacToe.printArray();
        
        
    }
    
public static boolean lookThroughArray(){
    
    // for(int r = 0; r < arr.length; r ++){
    //     for(int c = 0; c < arr[0].length; c ++){ 
            if(!arr[0][0].equals(TicTacToe.player1Symbol()) && !arr[0][0].equals(TicTacToe.player2Symbol()) || !arr[0][2].equals(TicTacToe.player1Symbol()) && !arr[0][2].equals(TicTacToe.player2Symbol()) || !arr[0][4].equals(TicTacToe.player1Symbol()) && !arr[0][4].equals(TicTacToe.player2Symbol()) || !arr[2][0].equals(TicTacToe.player1Symbol()) && !arr[2][0].equals(TicTacToe.player2Symbol()) || !arr[2][2].equals(TicTacToe.player1Symbol()) && !arr[2][2].equals(TicTacToe.player2Symbol()) || !arr[2][4].equals(TicTacToe.player1Symbol()) && !arr[2][4].equals(TicTacToe.player2Symbol()) || !arr[4][0].equals(TicTacToe.player1Symbol()) && !arr[4][0].equals(TicTacToe.player2Symbol()) || !arr[4][2].equals(TicTacToe.player1Symbol()) && !arr[4][2].equals(TicTacToe.player2Symbol()) || !arr[4][4].equals(TicTacToe.player1Symbol()) && !arr[4][4].equals(TicTacToe.player2Symbol())){
                return true;
        }
            // if(!arr[0][2].equals(TicTacToe.player1Symbol()) && !arr[0][2].equals(TicTacToe.player2Symbol()))
            //     return true;
            // if(!arr[0][4].equals(TicTacToe.player1Symbol()) && !arr[0][4].equals(TicTacToe.player2Symbol()))
            //     return true;
            // if(!arr[2][0].equals(TicTacToe.player1Symbol()) && !arr[2][0].equals(TicTacToe.player2Symbol()))
            //     return true;
            // if(!arr[2][2].equals(TicTacToe.player1Symbol()) && !arr[2][2].equals(TicTacToe.player2Symbol()))
            //     return true;
            // if(!arr[2][4].equals(TicTacToe.player1Symbol()) && !arr[2][4].equals(TicTacToe.player2Symbol()))
            //     return true;
            // if(!arr[4][0].equals(TicTacToe.player1Symbol()) && !arr[4][0].equals(TicTacToe.player2Symbol()))
            //     return true;
            // if(!arr[4][2].equals(TicTacToe.player1Symbol()) && !arr[4][2].equals(TicTacToe.player2Symbol()))
            //     return true;
            // if(!arr[4][4].equals(TicTacToe.player1Symbol()) && !arr[4][4].equals(TicTacToe.player2Symbol()))
            //     return true;    
        //     }
        // }
    return false;
    
}
    
public static void printArray(){
    
    for(int r = 0; r < arr.length; r ++){
            for(int c = 0; c < arr[0].length; c ++){ 
                System.out.print(arr[r][c] + " " );
            }
            System.out.println();
        }
}


public static String scanForSymbol1(){
    
    System.out.print("Player 1, choose your symbol: ");
    input = scan.nextLine();
    return input;
    
}

public static String player1Symbol(){
    
    String first = " " + input + " ";
    return first;
}

public static String scanForSymbol2(){
    
    System.out.print("Player 2, choose your symbol: ");
    input2 = scan.nextLine();
    return input2;
    
}

public static String player2Symbol(){
    
    String second = " " + input2 + " ";
    return second;
}

public static void checkSymbol(){
    
     while(TicTacToe.player1Symbol().equals(TicTacToe.player2Symbol())){
            System.out.print("Please do not choose the same symbol as Player 1. ");
            TicTacToe.scanForSymbol2();
        }
    
}    

public static String scanForPosition1(){
    
    System.out.print("Player 1, choose a position: ");
        pos1 = scan.nextLine();
        return pos1;
}

public static String player1Position(){
    
    String firstpos = pos1;
    return firstpos;
}

public static String scanForPosition2(){
    
    System.out.print("Player 2, choose a position: ");
        pos2 = scan.nextLine();
        return pos2;
}

public static String player2Position(){
    
    String secondpos = pos2;
    return secondpos;
}


public static void checkNumbers1(String pos){
    
        while(!pos.equals("1") && !pos.equals("2") && !pos.equals("3") && !pos.equals("4") && !pos.equals("5") && !pos.equals("6") && !pos.equals("7") && !pos.equals("8") && !pos.equals("9")){
          System.out.println("Please enter a valid position from numbers 1 - 9. ");
          pos = TicTacToe.scanForPosition1();
        }
        
}


public static void checkNumbers2(String pos){
    
        while(!pos.equals("1") && !pos.equals("2") && !pos.equals("3") && !pos.equals("4") && !pos.equals("5") && !pos.equals("6") && !pos.equals("7") && !pos.equals("8") && !pos.equals("9")){
          System.out.println("Please enter a valid position from numbers 1 - 9. ");
          pos = TicTacToe.scanForPosition2();
        }
        
}


public static void checkRepeatForP1(String pos, String otherPos){
    
        while(pos.equals(otherPos)){
          System.out.println("Please do not enter the same position as Player 2. ");
          pos = TicTacToe.scanForPosition1();
        }
        
}

public static void checkRepeatForP2(String pos, String otherPos){
    
        while(pos.equals(otherPos)){
          System.out.println("Please do not enter the same position as Player 1. ");
          pos = TicTacToe.scanForPosition2();
        }
        
}

public static boolean position1(String pos, String symbol){
  
        
        if((pos.equals("1") && !arr[0][0].equals(TicTacToe.player1Symbol())) && (pos.equals("1") && !arr[0][0].equals(TicTacToe.player2Symbol()))){
        
            arr[0][0]= symbol;
            return true;
        }
        else if((pos.equals("2") && !arr[0][2].equals(TicTacToe.player1Symbol())) && (pos.equals("2") && !arr[0][2].equals(TicTacToe.player2Symbol()))){
        
            arr[0][2]= symbol;
            return true;
    }
        else if((pos.equals("3") && !arr[0][4].equals(TicTacToe.player1Symbol())) && (pos.equals("3") && !arr[0][4].equals(TicTacToe.player2Symbol()))){
        
            arr[0][4]= symbol;
            return true;
        }
        else if((pos.equals("4") && !arr[2][0].equals(TicTacToe.player1Symbol())) && (pos.equals("4") && !arr[2][0].equals(TicTacToe.player2Symbol()))){
        
            arr[2][0]= symbol;
            return true;
        }
        else if((pos.equals("5") && !arr[2][2].equals(TicTacToe.player1Symbol())) && (pos.equals("5") && !arr[2][2].equals(TicTacToe.player2Symbol()))){
        
            arr[2][2]= symbol;
            return true;
        }
        else if((pos.equals("6") && !arr[2][4].equals(TicTacToe.player1Symbol())) && (pos.equals("6") && !arr[2][4].equals(TicTacToe.player2Symbol()))){
        
            arr[2][4]= symbol;
            return true;
        }
        else if((pos.equals("7") && !arr[4][0].equals(TicTacToe.player1Symbol())) && (pos.equals("7") && !arr[4][0].equals(TicTacToe.player2Symbol()))){
        
            arr[4][0]= symbol;
            return true;
        }
        else if((pos.equals("8") && !arr[4][2].equals(TicTacToe.player1Symbol())) && (pos.equals("8") && !arr[4][2].equals(TicTacToe.player2Symbol()))){
        
            arr[4][2]= symbol;
            return true;
        }
        else if((pos.equals("9") && !arr[4][4].equals(TicTacToe.player1Symbol())) && (pos.equals("9") && !arr[4][4].equals(TicTacToe.player2Symbol()))){
        
            arr[4][4]= symbol;
            return true;
        }
        
            return false;
}


public static boolean position2(String pos, String symbol){
        
        if((pos.equals("1") && !arr[0][0].equals(TicTacToe.player1Symbol())) && (pos.equals("1") && !arr[0][0].equals(TicTacToe.player2Symbol()))){
        
            arr[0][0]= symbol;
            return true;
        }
        else if((pos.equals("2") && !arr[0][2].equals(TicTacToe.player1Symbol())) && (pos.equals("2") && !arr[0][2].equals(TicTacToe.player2Symbol()))){
        
            arr[0][2]= symbol;
            return true;
    }
        else if((pos.equals("3") && !arr[0][4].equals(TicTacToe.player1Symbol())) && (pos.equals("3") && !arr[0][4].equals(TicTacToe.player2Symbol()))){
        
            arr[0][4]= symbol;
            return true;
        }
        else if((pos.equals("4") && !arr[2][0].equals(TicTacToe.player1Symbol())) && (pos.equals("4") && !arr[2][0].equals(TicTacToe.player2Symbol()))){
        
            arr[2][0]= symbol;
            return true;
        }
        else if((pos.equals("5") && !arr[2][2].equals(TicTacToe.player1Symbol())) && (pos.equals("5") && !arr[2][2].equals(TicTacToe.player2Symbol()))){
        
            arr[2][2]= symbol;
            return true;
        }
        else if((pos.equals("6") && !arr[2][4].equals(TicTacToe.player1Symbol())) && (pos.equals("6") && !arr[2][4].equals(TicTacToe.player2Symbol()))){
        
            arr[2][4]= symbol;
            return true;
        }
        else if((pos.equals("7") && !arr[4][0].equals(TicTacToe.player1Symbol())) && (pos.equals("7") && !arr[4][0].equals(TicTacToe.player2Symbol()))){
        
            arr[4][0]= symbol;
            return true;
        }
        else if((pos.equals("8") && !arr[4][2].equals(TicTacToe.player1Symbol())) && (pos.equals("8") && !arr[4][2].equals(TicTacToe.player2Symbol()))){
        
            arr[4][2]= symbol;
            return true;
        }
        else if((pos.equals("9") && !arr[4][4].equals(TicTacToe.player1Symbol())) && (pos.equals("9") && !arr[4][4].equals(TicTacToe.player2Symbol()))){
        
       
            arr[4][4]= symbol;return true;
        }
            return false;

}


public static boolean checkWin(){
    if(arr[0][0].equals(TicTacToe.player1Symbol()) && arr[0][2].equals(TicTacToe.player1Symbol()) && arr[0][4].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[2][0].equals(TicTacToe.player1Symbol()) && arr[2][2].equals(TicTacToe.player1Symbol()) && arr[2][4].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[4][0].equals(TicTacToe.player1Symbol()) && arr[4][2].equals(TicTacToe.player1Symbol()) && arr[4][4].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[0][0].equals(TicTacToe.player1Symbol()) && arr[2][2].equals(TicTacToe.player1Symbol()) && arr[4][4].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[0][4].equals(TicTacToe.player1Symbol()) && arr[2][2].equals(TicTacToe.player1Symbol()) && arr[4][0].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[0][0].equals(TicTacToe.player1Symbol()) && arr[2][0].equals(TicTacToe.player1Symbol()) && arr[4][0].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[0][2].equals(TicTacToe.player1Symbol()) && arr[2][2].equals(TicTacToe.player1Symbol()) && arr[4][2].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[0][4].equals(TicTacToe.player1Symbol()) && arr[2][4].equals(TicTacToe.player1Symbol()) && arr[4][4].equals(TicTacToe.player1Symbol())){
        return true;
    }
    else if(arr[0][0].equals(TicTacToe.player2Symbol()) && arr[0][2].equals(TicTacToe.player2Symbol()) && arr[0][4].equals(TicTacToe.player2Symbol())){
        return true;
    }
    else if(arr[2][0].equals(TicTacToe.player2Symbol()) && arr[2][2].equals(TicTacToe.player2Symbol()) && arr[2][4].equals(TicTacToe.player2Symbol())){
        return true;
    }
    else if(arr[4][0].equals(TicTacToe.player2Symbol()) && arr[4][2].equals(TicTacToe.player2Symbol()) && arr[4][4].equals(TicTacToe.player2Symbol())){
        return true;
    }
    else if(arr[0][0].equals(TicTacToe.player2Symbol()) && arr[2][2].equals(TicTacToe.player2Symbol()) && arr[4][4].equals(TicTacToe.player2Symbol())){
        return true;
    }
    else if(arr[0][4].equals(TicTacToe.player2Symbol()) && arr[2][2].equals(TicTacToe.player2Symbol()) && arr[4][0].equals(TicTacToe.player2Symbol())){
        return true;
    }
    else if(arr[0][0].equals(TicTacToe.player2Symbol()) && arr[2][0].equals(TicTacToe.player2Symbol()) && arr[4][0].equals(TicTacToe.player2Symbol())){
        return true;
    }
    else if(arr[0][2].equals(TicTacToe.player2Symbol()) && arr[2][2].equals(TicTacToe.player2Symbol()) && arr[4][2].equals(TicTacToe.player2Symbol())){
        return true;
    }
    else if(arr[0][4].equals(TicTacToe.player2Symbol()) && arr[2][4].equals(TicTacToe.player2Symbol()) && arr[4][4].equals(TicTacToe.player2Symbol())){
        return true;
    }
    return false;
    }
    
public static void reset(){
    
    arr[0][0] = " 1 ";
    arr[0][2] = " 2 ";
    arr[0][4] = " 3 ";
    arr[2][0] = " 4 ";
    arr[2][2] = " 5 ";
    arr[2][4] = " 6 ";
    arr[4][0] = " 7 ";
    arr[4][2] = " 8 ";
    arr[4][4] = " 9 ";
    
}    
    
public static void play(){    
    
    
        TicTacToe.printNewBoard();
        TicTacToe.scanForSymbol1();
        TicTacToe.scanForSymbol2();
        TicTacToe.checkSymbol();
    
    
    while(TicTacToe.checkWin() != true){      
            TicTacToe.scanForPosition1();
            TicTacToe.checkNumbers1(TicTacToe.player1Position());
            TicTacToe.checkRepeatForP1(TicTacToe.player1Position(),TicTacToe.player2Position());
            while(TicTacToe.position1(TicTacToe.player1Position(),TicTacToe.player1Symbol()) == false){
                System.out.println("Please choose a position that has not been selected yet.");
                TicTacToe.scanForPosition1();
            }
            if(TicTacToe.checkWin() == true){ 
                    System.out.println("Congratulations! Player 1 has won!");
                    break;
                    }
            
            TicTacToe.printArray();
            TicTacToe.checkWin();
                
    if(TicTacToe.lookThroughArray() == true){
            if(TicTacToe.checkWin() == true){ 
                    System.out.println("Congratulations! Player 1 has won!");
                    break;
                    }
            else{
                    TicTacToe.scanForPosition2();
                    TicTacToe.checkNumbers2(TicTacToe.player2Position());
                    TicTacToe.checkRepeatForP2(TicTacToe.player2Position(),TicTacToe.player1Position());
                    while(TicTacToe.position2(TicTacToe.player2Position(),TicTacToe.player2Symbol())== false){
                        System.out.println("Please choose a position that has not been selected yet.");
                        TicTacToe.scanForPosition2();
                    }
                    TicTacToe.printArray();
                    TicTacToe.checkWin();
                        if(TicTacToe.checkWin() == true){
                         System.out.println("Congratulations! Player 2 has won!");
                         break;
                }
            }
        }
    else{        
            System.out.println("Tie! Better luck next time!");
            break;
            }
        }
    
    
}
    
    
    
    
    
}
