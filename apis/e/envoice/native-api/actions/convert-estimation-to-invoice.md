# Convert Estimation to Invoice with Envoice

Converts an estimation to an invoice in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `estimation/convert`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Convert Estimation to Invoice](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Estimation identifier to convert to an invoice. |
