# Lab Report 2
## Part 1

- I implemented a web server that was able to add strings to a list, and returned all strings that contained a given substring to search for.

- The following code is from the SearchEngine.java file:

```
import java.io.IOException; 
import java.net.URI; 
import java.util.ArrayList;

class Handler implements URLHandler { 
    ArrayList<String> words = new ArrayList<String>();

    public String handleRequest(URI url) {
        System.out.println("Path: " + url.getPath());
        if (url.getPath().contains("/add")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                words.add(0, parameters[1]);
                return parameters[1] + " added";
            }
        }
        else if(url.getPath().contains("/search")){
            String[] parameters = url.getQuery().split("=");
            ArrayList<String> chosenWords = new ArrayList<String>();
            if (parameters[0].equals("s")){
                for(int i = 0; i < words.size(); i++){
                    if(words.get(i).contains(parameters[1])){
                        chosenWords.add(0, words.get(i));
                    }
                }
            }
            return chosenWords.toString();
        }
         else if (url.getPath().equals("/")) {
            return "Please add a word or search with keywords!";
         }
        else{
            return "404 Not Found!";
        }
        return "";
    }
}


class SearchEngine{
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
- If the URL path contains `add`, it will initiate the command to add a string value to an arraylist. 

    - In this following image, I use the `add` command which takes the String value, `apple`, as an argument.

    ![AddMethodDemoApple](SearchAddDemo.png)
    
    - In the next image, I use the `add` command twice with `pineapple` and `randomstring` as my arguments.

    ![AddMethodDemoPineapple](SearchAddDemoPineapple.png)
    ![AddMethodDemoRandom](SearchAddDemoRandom.png)

- If the URL path contains `search`, it will search from the indicated substring through the list of added words, and then return the strings with the substring.

    - In the following image, I use the `search` command with the substring argument, `apple`, and the output is shown to be `[apple, pineapple]`, which are both of the words that contain the substring.

    ![SearchMethodDemo](SearchMethodDemo.png)

## Part 2

### Array
