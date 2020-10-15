const suits = ['hearts', 'diamonds', 'clubs', 'spades']
const ranks = [
  'ace',
  'two',
  'three',
  'four',
  'five',
  'six',
  'seven',
  'eight',
  'nine',
  'ten',
  'jack',
  'queen',
  'king',
]
// Freezing these arrays so the order can't be changed
Object.freeze(suits)
Object.freeze(ranks)

const createCard = (rank = '') => {
  if (!ranks.includes(rank.toLowerCase())) {
    return 'Invalid rank'
  }
  return suits.map(suit => ({
    rank,
    suit,
  }))
}

console.log(createCard('Ace')) // should create
console.log(createCard('something')) //should fail

const createDeck = _ => {
  const cards = ranks.map(rank => createCard(rank))
  return cards.flat()
}
const deck = createDeck()
console.log(deck) // should return an array of cards

const cardPosition = card => {
  const positionOfRankInRanks = ranks.indexOf(card.rank) + 1
  const positionOfSuitInSuits = suits.indexOf(card.suit)
  const result = 4 * positionOfRankInRanks - (4 - positionOfSuitInSuits)
  return result
}

const aceOfSpades = {
  rank: 'ace',
  suit: 'spades',
}

const sevenOfSpades = {
  rank: 'seven',
  suit: 'spades',
}

const eightOfHearts = {
  rank: 'eight',
  suit: 'hearts',
}

const queenOfDiamonds = {
  rank: 'queen',
  suit: 'diamonds',
}

console.log(cardPosition(aceOfSpades))
console.log(cardPosition(sevenOfSpades))
console.log(cardPosition(eightOfHearts))
console.log(cardPosition(queenOfDiamonds))

console.log(deck[3])
console.log(deck[27])
console.log(deck[28])
console.log(deck[45])
