# Update Tax Rate with Envoice

Updates an existing tax rate in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `tax/update`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Update Tax Rate](https://github.com/EmitKnowledge/Envoice/blob/master/tax.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Tax rate ID. |
| `Name` | body | `string` | yes | Tax rate name. |
| `Percentage` | body | `number` | yes | Tax percentage value. |
