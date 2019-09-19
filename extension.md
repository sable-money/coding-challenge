#

Extension:

The fraud department is very happy with the work, however, they have realised that there is an incredibly large amount of work in reviewing transactions.

They have now developed a heuristic to automatically blocked transactions based upon the following heuristic:

If a transaction from Person A -> Person B is blocked, then all subsequent transactions from person B are blocked. 

Diagram:

![extension](https://i.imgur.com/LIm2Gzt.png "Showing what transactions should be blocked")

Here is a sample of transactions that should be reviewed:

```json
[
  {
    "id": 1,
    "userId": "A",
    "recipientId": "B",
    "amount": "$100",
    "status": "none"
  },
  {
    "id": 2,
    "userId": "B",
    "recipientId": "C",
    "amount": "$80",
    "status": "none"
  },
  {
    "id": 3,
    "userId": "D",
    "recipientId": "E",
    "amount": "$900",
    "status": "none"
  },
  {
    "id": 4,
    "userId": "A",
    "recipientId": "E",
    "amount": "$187",
    "status": "none"
  },
  {
    "id": 5,
    "userId": "E",
    "recipientId": "F",
    "amount": "$98",
    "status": "none"
  },
  {
    "id": 6,
    "userId": "G",
    "recipientId": "G",
    "amount": "$170",
    "status": "none"
  },
  {
    "id": 7,
    "userId": "G",
    "recipientId": "A",
    "amount": "$100",
    "status": "none"
  },
  {
    "id": 8,
    "userId": "A",
    "recipientId": "B",
    "amount": "$3400",
    "status": "none"
  },
  {
    "id": 9,
    "userId": "F",
    "recipientId": "G",
    "amount": "$3400",
    "status": "none"
  },
  {
    "id": 10,
    "userId": "D",
    "recipientId": "E",
    "amount": "$3400",
    "status": "none"
  },
  {
    "id": 11,
    "userId": "B",
    "recipientId": "F",
    "amount": "$3400",
    "status": "none"
  },
  {
    "id": 12,
    "userId": "C",
    "recipientId": "B",
    "amount": "$3400",
    "status": "none"
  }
]
```
