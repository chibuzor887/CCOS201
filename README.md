import java.math.BigInteger;

public class Fibonacci {
    public static void main(String[] args) {
        // BigInteger is needed because F(93) and beyond overflow a long
        BigInteger a = BigInteger.ZERO; // F(0)
        BigInteger b = BigInteger.ONE;  // F(1)

        // Print the first 100 numbers: F(0) through F(99)
        for (int i = 0; i < 100; i++) {
            System.out.println("F(" + i + ") = " + a);

            // Next number is the sum of the previous two
            BigInteger next = a.add(b);

            // Shift forward: a becomes the old b, b becomes the new sum
            a = b;
            b = next;
        }
    }
}
