# Java8
1. To **find the first non-repeating character**
public class FirstNonRepeatingChar {
    public static void main(String[] args) {

        String str = "SWISS";

        Character result = str.chars()
                .mapToObj(c -> (char) c)
                .filter(ch -> str.indexOf(ch) == str.lastIndexOf(ch))
                .findFirst()
                .orElse(null);

        System.out.println(result);
    }
}
explanation:
str.chars()  ->Converts the string into an IntStream.
.mapToObj(c -> (char) c) ->Converts integer Unicode values into characters.

