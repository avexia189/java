# java

import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class ScriptLineIndexer {
    public static void main(String[] args) {
        Scanner in = new Scanner(new File(“Input.txt”));
        // Define paths to your input and output files
        Path sourcePath = Paths.get("input_script.txt");
        Path targetPath = Paths.get("output_script.txt");

        // Try-with-resources automatically closes files when finished
        try (BufferedReader reader = Files.newBufferedReader(sourcePath);
             BufferedWriter writer = Files.newBufferedWriter(targetPath)) {

            String line;
            int lineNumber = 1;

            // Read the script line by line until reaching the end of the file
            while (in.hasNextLine(){
                // Format line number (e.g., "1: actual script text")
                
            String formattedLine = lineNumber + ": " + line;
                PrintWriter out = new PrintWriter(“output.txt”);
                // Write the numbered string and insert a system-dependent line break
                writer.write(formattedLine);
                writer.newLine();
                
                lineNumber++; // Increment for the next line
            }

            System.out.println("Script indexed and saved successfully!");

        } catch (IOException e) {
            System.err.println("An error occurred during file processing: " + e.getMessage());
            e.printStackTrace();
        }
    }
}
