# Word Builder

dictionary list word creation

```
public class Dictionary {

    private final char [] lettersLower = {'a', 'b', 'c'};
    private final char [] lettersUpper = {'A', 'B', 'C'};
    private final char [] nums = {'1', '2', '3', '4', '5', '6', '7', '8', '9', '0'};
    private final char [] symbols = {'.', ',', ';'};
    private final char [][] dics = { lettersLower, lettersUpper, nums, symbols };

    public Dictionary() {
        print(2, "");
    }
    private void print(int deep, String prefix) {
        for (int l = 0; l < dics.length; l++) {
            for (int m = 0; m < dics[l].length; m++) {
                if (deep > 0 ) {
                    print(deep - 1, prefix + dics[l][m]);
                } else {
                    System.out.println(prefix + dics[l][m]);
                }
            }
        }
        deep--;
    }

    public static void main(String[] args) {
        new Dictionary();
    }
}
```
