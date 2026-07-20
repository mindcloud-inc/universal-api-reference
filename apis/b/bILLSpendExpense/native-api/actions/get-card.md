# Get Card with BILL Spend & Expense

Retrieves a vendor card from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/cards/:cardId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Get Card](https://developer.bill.com/reference/getcard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | BILL-generated ID or UUID of the card. |
