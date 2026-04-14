# atividade-13-04
public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite o número de linhas (n): ");
        int n = scanner.nextInt();
        
        System.out.print("Digite o número de colunas (m): ");
        int m = scanner.nextInt();

        int[][] matriz = new int[n][m];
        int[][] transposta = new int[m][n];

        System.out.println("\nDigite os valores para a matriz:");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                System.out.printf("Elemento [%d][%d]: ", i, j);
                matriz[i][j] = scanner.nextInt();
                
                transposta[j][i] = matriz[i][j];
            }
        }

        System.out.println("\n--- Matriz Original (" + n + "x" + m + ") ---");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                System.out.print(matriz[i][j] + "\t");
            }
            System.out.println();
        }

        System.out.println("\n--- Matriz Transposta (" + m + "x" + n + ") ---");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print(transposta[i][j] + "\t");
            }
            System.out.println();
        }

        scanner.close();
    }
}
