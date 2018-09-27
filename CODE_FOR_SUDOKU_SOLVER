#code for the problem
class Sudoku
{
    private int[][] sudoku;
    private static final int UNASSIGNED = 0;
      
    public Sudoku()
    {
        sudoku = new int[9][9];
    }
      
    public Sudoku(int sudoku[][])
    {
        this.sudoku= sudoku;
    }
      
    
    //private boolean CIR(int row,int NUM){...}
    //private boolean CIC(int col,int NUM){...}
    //private boolean CIB(int row, int col,int NUM){...}
    //private boolean isAllowed(int row, int col,int NUM){...}
    //public void display_Sudoku(){...}
    //public boolean solve_Sudoku(){...}
}
private boolean CIR(int row,int NUM)  //TO CHECK NO. IN ROW
{
    for(int i=0;i<9;i++)
    {
        if(sudoku[row][i]==NUM)
        {
            return true;
        }
    }
    return false;
}
  
 
  
private boolean CIC(int col,int NUM)//TO CHECK NO. IN COL
{
    for(int i=0;i<9;i++)
    {
        if(sudoku[i][col]==NUM)
        {
            return true;
        }
    }
    return false;
}
  
  
private boolean CIB(int row, int col,int NUM)////TO CHECK NO. IN 3*3 BOX
{
    int r = row - row%3;
    int c = col - col%3;
    for(int i = r ; i< r+3 ; i++)
    {
        for(int j = c; j < c+3 ; j++)
        {
            if(sudoku[i][j]==NUM)
            {
                return true;
            }
        }
          
    }
    return false;
}private boolean isAllowed(int row, int col,int NUM)
{
    return !(CIR(row, NUM) || CIC(col, NUM) || CIB(row, col, NUM));
}
public boolean solve_Sudoku()
{
    for(int row=0;row<9;row++)
    {
        for(int col=0;col<9;col++)
        {
            if(sudoku[row][col]==UNASSIGNED)
            {
                for(int NUM=1;NUM<=9;NUM++)
                {
                    if(isAllowed(row, col, NUM))
                    {
                        sudoku[row][col] = NUM;
                        if(solve_Sudoku())
                        {
                            return true;
                        }
                        else
                        {
                            sudoku[row][col] = UNASSIGNED;
                        }
                    }
                }
                return false;
            }
        }
    }
    return true;
}
public void display_Sudoku()
{
    for(int i=0;i<9;i++)
    {
        if(i%3==0 && i!=0)
        {
            System.out.println("----------------------------------\n");
        }
        for(int j=0;j<9;j++)
        {
            if(j%3==0 && j!=0)
            {
                System.out.print(" | ");
            }
            System.out.print(" " + sudoku[i][j] + " ");
  
        }
  
        System.out.println();
    }
    System.out.println("\n\n__________________________________________\n\n");
}
