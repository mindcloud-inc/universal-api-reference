# Delete Invoice with CoachAccountable

Deletes an invoice from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Delete Invoice](https://www.coachaccountable.com/APIDocs#Invoice.delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceID` | body | `number` | yes | The ID of the Invoice to be deleted. Invoice Number also accepted when prefixed with a "#", e.g. "#1005". |
