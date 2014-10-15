public class Shorty {
    public static final String ALPHABET = "23456789abcdfghjkmnpqrstvwxyzBCDFGHJKLMNOPQRSTVWXYZ";
    public static final String REVERSE_ALPHABET = "ZYXWVTSRQPONMLKJHGFDCBzyxwvtsrqpnmkjhgfdcba98765432";
    public static final int BASE = ALPHABET.length();

    public static String encode(String url) {
        int num = url.hashCode();
        StringBuilder str = new StringBuilder();
        if (num < 0) {
            while (num < 0) {
                str.insert(0, REVERSE_ALPHABET.charAt(-num % BASE));
                num = num / BASE;
            }
        } else {
            while (num > 0) {
                str.insert(0, ALPHABET.charAt(num % BASE));
                num = num / BASE;
            }
        }
        return str.toString();
    }
}
