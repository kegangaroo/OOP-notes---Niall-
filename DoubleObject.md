#Two objects being put one after the other

```python

from random import shuffle as r_shuffle

class Card:
    def __init__(self, suit, value):
        self.suit = suit
        self.value = value

    def __str__(self):
        value = self.value
        if self.value == 11:
            value = "Jack"
        elif self.value == 12:
            value = "Queen"
        elif self.value == 13:
            value = "King"
        elif self.value == 14:
            value = "Ace"

        return f"{value} of {self.suit}"

    def __repr__(self):
        return self.__str__()

#takes the input of the given card, and reformats the input if the vaule has a name, or it remains a number, and phrases it in sentence format

class Deck:
    __SUITS = ['Spades', 'Hearts', 'Clubs', 'Diamonds']
    __VALUES = list(range(2, 15))

    def __init__(self):
        self.deck = self.initial_deck()

    def initial_deck(self):
        result = []
        for suit in self.__SUITS:
            for value in self.__VALUES:
                result.append(Card(suit, value))
        return result

    def shuffle(self):
        if self.deck:
            r_shuffle(self.deck)
            return True
        else:
            print('We have no cards in our deck')
            return False

    def draw(self):
        if self.deck:
            return self.deck.pop()
        else:
            print('We have no cards in our deck')
            return None

#is given the inputs to create an entire deck of cards
#to rearrange the list, the shuffle function sorts them at random as they are added to the list in order of the suits as they are listed
#finally, the draw function, takes certain cards out, adding them to the empty list, creating the hand the user recieves back

```

##Dual Object
- the first object sets the format and characteristics
- the second object is when you have multiple of that object, and how they can be manipulated or changed
- the defining of a function within an object allows for the desired manipulation and proper output the "programmer" is looking for
