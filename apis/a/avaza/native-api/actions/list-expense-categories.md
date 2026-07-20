# List Expense Categories with Avaza

Retrieves expense categories from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ExpenseCategory`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Expense Categories](https://api.avaza.com/#!/ExpenseCategory/ExpenseCategory_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isEnabled` | query | `boolean` | no | Optional filter on for enabled/disabled categories. Defaults to true. |
