import java.util.List;
import java.util.Arrays;

public class Card implements Comparable<Card> {
    private String name; // Ace, 2, ..., King
    private String suit; // Hearts, Clubs, Diamonds, Spades

    // Define New Deck Order hierarchies to assign numerical weights
    private static final List<String> RANK_ORDER = Arrays.asList(
            "Ace", "2", "3", "4", "5", "6", "7", "8", "9", "10", "Jack", "Queen", "King"
    );
    private static final List<String> SUIT_ORDER = Arrays.asList(
            "Hearts", "Clubs", "Diamonds", "Spades"
    );

    public Card(String name, String suit) {
        this.name = name;
        this.suit = suit;
    }

    // Getters and Setters
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }

    public String getSuit() { return suit; }
    public void setSuit(String suit) { this.suit = suit; }

    @Override
    public String toString() {
        return name + " of " + suit;
    }

    @Override
    public int compareTo(Card other) {
        // 1. Compare the Suit first (Hearts -> Clubs -> Diamonds -> Spades)
        int thisSuitWeight = SUIT_ORDER.indexOf(this.suit);
        int otherSuitWeight = SUIT_ORDER.indexOf(other.suit);

        if (thisSuitWeight != otherSuitWeight) {
            return thisSuitWeight - otherSuitWeight;
        }

        // 2. If Suits are the same, compare by Rank (Ace -> King)
        int thisRankWeight = RANK_ORDER.indexOf(this.name);
        int otherRankWeight = RANK_ORDER.indexOf(other.name);

        return thisRankWeight - otherRankWeight;
    }
}
