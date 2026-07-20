# Send Invoice Email with Refrens

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:urlKey/invoices/:invoiceID/email`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Send Invoice Email](https://help.refrens.com/en/article/how-to-trigger-emails-for-all-your-documents-via-api-1khpmic/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceID` | path | `string` | yes | — |
| `to` | body | `object` | yes | Recipient object with email and optional name. |
| `cc[]` | body | `array<object>` | no | — |
| `from` | body | `object` | no | Optional sender object. Refrens requires the sender email to be connected in Refrens before use. |
