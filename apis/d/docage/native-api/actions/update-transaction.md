# Update Transaction with Docage

Updates an existing transaction in Docage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Transactions/:id`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [Update Transaction](https://documentation.docage.com/modifier-un-parcours-23707883e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Docage transaction ID. |
| `IsTest` | body | `boolean` | no | Whether the updated transaction remains a test. |
| `Name` | body | `string` | no | The updated transaction name. |
| `Reminder` | body | `number` | no | Reminder cadence enum value: 0, 1, 2, 7, 14, or 30. |
