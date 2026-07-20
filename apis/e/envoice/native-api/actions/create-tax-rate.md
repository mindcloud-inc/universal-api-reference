# Create Tax Rate with Envoice

Creates a new tax rate in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `tax/new`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Create Tax Rate](https://github.com/EmitKnowledge/Envoice/blob/master/tax.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Tax rate name. |
| `Percentage` | body | `number` | yes | Tax percentage value. |
