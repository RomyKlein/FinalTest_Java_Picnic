import java.io.File;
import java.io.FileInputStream;
import java.util.*;

public class Fruits {
    String words;
    int count;
    String longestWord = "";
    String currentWord;

    public Fruits ()

    {

        File fileFruits = new File("input.txt");
        try (Scanner scannerWords = new Scanner(new FileInputStream(fileFruits))) {
            count = 0;
            while (scannerWords.hasNext()) {
                scannerWords.next();
                count++;
            }
            System.out.println("Number of words in file: " + count);
        } catch (Exception exception) {
            System.out.println("oops!");
        }

    }

    public String longestWord () {
        try (Scanner scannerWords = new Scanner(new File("input.txt"))) {
            while (scannerWords.hasNext()) {
                currentWord = scannerWords.next();

                if ((currentWord.length() > longestWord.length()) && (!currentWord.matches(".*\\d.*")))
                {
                    longestWord = currentWord;
                }

            }
            System.out.println("The longest word is " + longestWord);

        }

        catch (Exception ex) {
            System.out.println("oops!");
        }
        return longestWord;

    }

    public void sameWords () {
        HashMap<String, Integer> countEachWord = new HashMap<>();
        try (Scanner scannerWords = new Scanner(new File("input.txt"))) {
            while (scannerWords.hasNext()) {
                words = scannerWords.next();
                if (countEachWord.containsKey(words)) {
                    countEachWord.put(words, countEachWord.get(words) + 1);
                }
                else {
                    countEachWord.put(words, 1);
                }
            }
            for (Map.Entry<String, Integer> outPut : countEachWord.entrySet()) {
                System.out.println("Number of fruit/vegetable: " + outPut.getKey() + " " + outPut.getValue());
            }
        }
        catch (Exception exception) {
            System.out.println("OOPS!");
        }

    }
}


public class Main {
    public static void main(String[] args) {
        Fruits fruits = new Fruits();
        fruits.longestWord();
        fruits.sameWords();
    }
}
