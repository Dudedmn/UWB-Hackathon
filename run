import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;
import java.io.StringWriter;
import java.util.*;

public class run {

	private final static String OUTPUT = "Server.txt";
	private final static String INPUT = "Client.txt";

	public static void main(String[] args) throws IOException{

		Canvas testCanvas = new Canvas(250,250,50,30,1,1);

		//the player
		char[][] player1 = new char[3][2];
		player1[0][0] = '.';
		player1[0][1] = ' ';
		player1[1][1] = '-';
		player1[2][0] = '.';
		player1[2][1] = ' ';
		player1[1][0] = ' ';
		GameObject playerOne = new MainPlayer(player1, 3,2,25,1);

		char[][] enemy1 = new char[3][2];
		enemy1[0][0] = '@';
		enemy1[0][1] = ' ';
		enemy1[1][1] = 'V';
		enemy1[2][0] = '@';
		enemy1[2][1] = ' ';
		enemy1[1][0] = ' ';
		GameObject enemyOne = new MainPlayer(enemy1, 3,2,10,18);

//		char[][] enemy2 = new char[3][2];
//		enemy2[0][0] = '@';
//		enemy2[0][1] = ' ';
//		enemy2[1][1] = 'V';
//		enemy2[2][0] = '@';
//		enemy2[2][1] = ' ';
//		enemy2[1][0] = ' ';
//		GameObject enemyTwo = new MainPlayer(enemy2, 3,2,1,1);

		char[][] tree1 = new char[7][4];
		tree1[0][0] = '└';
		tree1[1][0] = '|';
		tree1[2][0] = 'ಠ';
		tree1[3][0] = '‸';
		tree1[4][0] = 'ಠ';
		tree1[5][0] = '|';
		tree1[6][0] = '┘';
		tree1[0][1] = ' ';
		tree1[1][1] = '|';
		tree1[2][1] = ' ';
		tree1[3][1] = ' ';
		tree1[4][1] = ' ';
		tree1[5][1] = '|';
		tree1[6][1] = ' ';
		tree1[0][2] = ' ';
		tree1[1][2] = '|';
		tree1[2][2] = ' ';
		tree1[3][2] = ' ';
		tree1[4][2] = ' ';
		tree1[5][2] = '|';
		tree1[6][2] = ' ';
		tree1[0][3] = ' ';
		tree1[1][3] = '|';
		tree1[2][3] = ' ';
		tree1[3][3] = ' ';
		tree1[4][3] = ' ';
		tree1[5][3] = '|';
		tree1[6][3] = ' ';
		GameObject treeOne = new MainPlayer(tree1, 7,4,35,21);

		testCanvas.addFG(treeOne);
		testCanvas.addMG(enemyOne);
		//testCanvas.addMG(enemyOne);
		testCanvas.addBG(playerOne);

		stringWriter(testCanvas.Render(), OUTPUT);
		while(true){
			char curr = stringReader(INPUT);
			if(curr != 0) {
				treeOne.moveGridBased(curr);
				stringWriter(testCanvas.Render(), OUTPUT);
			}
		}

	}

	public static char stringReader(String filename) {
		try {
			BufferedReader br = new BufferedReader(new FileReader(filename));
			char result = br.readLine().charAt(0);
			br.close();

			BufferedWriter writer = new BufferedWriter(new FileWriter(filename));
			writer.close();
			return result;
		}
		catch (Exception e){
			return 0;
		}
	}

	public static void stringWriter(String toWrite, String fileName) throws IOException {
		BufferedWriter writer = new BufferedWriter(new FileWriter(fileName));
		writer.write(toWrite);
		writer.close();
	}

}
