# Get Invoice with CoachAccountable

Retrieves an invoice from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Get Invoice](https://www.coachaccountable.com/APIDocs#Invoice.get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceID` | body | `number` | no | The ID of the Invoice to be updated. Invoice Number also accepted when prefixed with a "#", e.g. "#1005". |
