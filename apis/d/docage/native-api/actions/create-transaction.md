# Create Transaction with Docage

Creates a new transaction in Docage.

## Endpoint

- **Method:** `POST`
- **Path:** `/Transactions`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [Create Transaction](https://documentation.docage.com/cr%C3%A9er-un-parcours-seul-23707899e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IsTest` | body | `boolean` | yes | Whether to create the transaction as a test. |
| `Name` | body | `string` | yes | The transaction name. |
| `Reminder` | body | `number` | yes | Reminder cadence enum value: 0, 1, 2, 7, 14, or 30. |
