# Send Invoice with CoachAccountable

Sends an invoice from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Send Invoice](https://www.coachaccountable.com/APIDocs#Invoice.send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceID` | body | `number` | yes | The ID of the Invoice to be sent. Invoice Number also accepted when prefixed with a "#", e.g. "#1005". |
| `sendTo` | body | `list` | no | If not supplied, will send to the client. By supplying a valid email address this call can send to any 3rd party. Accepted values: `C`, `L`, `someone@example.com`. |
| `message` | body | `string` | no | An optional message to include as part of the invoice. |
