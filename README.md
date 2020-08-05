# card-deck-test

A very generic express application that exposes two restful APIs for cards. Originally intended for creating restful interface for **indian poker (teen patti)**.

Behind the scene it forwards the requests to https://deckofcardsapi.com

## Run

```bash=
npm install
npm start
```

## What does it do

It exposes the following APIs

1. GET `/card-deck/shuffle`

Returns

```
{
"success": true,
"deck_id": "9yw2kuc2we9a",
"remaining": 52,
"shuffled": true
}
```

2. GET `/card-deck/draw/:deck_id` where `deck_id` is returned in shuffle request

Returns

```javascript
{
  "success": true,
  "deck_id": "xb2p6m87l5oz",
  "cards": [
    {
      "code": "2H",
      "image": "https://deckofcardsapi.com/static/img/2H.png",
      "images": {
        "svg": "https://deckofcardsapi.com/static/img/2H.svg",
        "png": "https://deckofcardsapi.com/static/img/2H.png"
      },
      "value": "2",
      "suit": "HEARTS"
    },
    {
      "code": "8H",
      "image": "https://deckofcardsapi.com/static/img/8H.png",
      "images": {
        "svg": "https://deckofcardsapi.com/static/img/8H.svg",
        "png": "https://deckofcardsapi.com/static/img/8H.png"
      },
      "value": "8",
      "suit": "HEARTS"
    },
    {
      "code": "4S",
      "image": "https://deckofcardsapi.com/static/img/4S.png",
      "images": {
        "svg": "https://deckofcardsapi.com/static/img/4S.svg",
        "png": "https://deckofcardsapi.com/static/img/4S.png"
      },
      "value": "4",
      "suit": "SPADES"
    }
  ],
  "remaining": 49
}
```
