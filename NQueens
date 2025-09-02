package src;
public class NQueens {
    static int N = 8;
    static int[] board = new int[8];
    static int tablero = 0;

    // Imprime el tablero con las reinas
    static void printBoard() {
        System.out.println("intento: " + tablero);
        for (int i = 0; i < N; i++) {
            for (int j=0;j<N;j++){
                if (board[i]==j){
                    System.out.print("Q ");
                } else {
                    System.out.print(". ");
                }
            }
            System.out.println();
        }
        System.out.println();
    }

    /**
     * Resuelve la colocación de reinas usando backtracking
     * @param row 
     */
    public static void solve(int row) {
        if (row == N) {
            // Si llegamos al final, imprimir solución
            printBoard();
            return;
        }

        for (int col = 0; col < N; col++) {
            if (isSafe(row, col)) {
                board[row] = col; // Coloca reina
                solve(row + 1);   // Llama recursivamente
            }
        }
    }

    /**
     * Verifica si es seguro poner una reina en (row, col)
     */
    static boolean isSafe(int row, int col) {
        for (int i = 0; i < row; i++) {
            // Misma columna
            if (board[i] == col) return false;
            // Misma diagonal
            if (Math.abs(board[i] - col) == Math.abs(row - i)) return false;
        }
        return true;
    }

    // Método principal
    public static void main(String[] args) {
        solve(0);
    }
}
