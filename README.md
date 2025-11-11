# Poker65
Python library for working with poker hands

## Example

```py
from Poker65.card import Card
from Poker65.hands import get_best_hand

# 4 of spades and 10 of clubs
hand = [Card(suit='S', rank='4'), Card(suit='C', rank='T')]

community_cards = [
    Card(suit='H', rank='9'), # 9 of hearts
    Card(suit='S', rank='2'), # 2 of spades
    Card(suit='C', rank='J'), # Jack of clubs
    Card(suit='H', rank='7'), # 7 of hearts
    Card(suit='D', rank='8'), # 8 of diamonds
]

# ♣J, ♣T, ♡9, ♢8, ♡7
print(get_best_hand(hand + community_cards))
# Straight(♣J, ♣T, ♡9, ♢8, ♡7) 
print(repr(get_best_hand(hand + community_cards)))
```
