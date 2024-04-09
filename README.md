# Cash-Register
Cash Register

This is a JavaScript function to calculate the change and the state of a cash register for a given purchase price, cash tendered, and available cash in drawer (cid).

## Description

The `checkCashRegister()` function calculates the change due to a customer and the state of the cash register after a purchase. It takes three parameters: the purchase price (`price`), the cash given by the customer (`cash`), and the cash in drawer (`cid`). The function returns an object with two properties: `status` and `change`.

- The `status` property indicates the state of the cash register. It can have three values:
  - `"OPEN"`: There is enough cash in the drawer to provide change for the transaction.
  - `"CLOSED"`: The cash in the drawer is exactly equal to the change due, meaning the register is closed.
  - `"INSUFFICIENT_FUNDS"`: There is not enough cash in the drawer to provide the necessary change.

- The `change` property is an array representing the change due. Each element of the array is an array with two elements: the denomination of the currency (e.g., "QUARTER", "ONE"), and the amount of that currency to return.

## Usage

To use the `checkCashRegister()` function, call it with the purchase price, cash given, and the cash in drawer as parameters. For example:

```javascript
console.log(checkCashRegister(19.5, 20, [["PENNY", 1.01], ["NICKEL", 2.05], ["DIME", 3.1], ["QUARTER", 4.25], ["ONE", 90], ["FIVE", 55], ["TEN", 20], ["TWENTY", 60], ["ONE HUNDRED", 100]]));
