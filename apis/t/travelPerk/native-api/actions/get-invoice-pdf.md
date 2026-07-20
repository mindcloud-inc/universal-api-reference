# Get Invoice PDF with TravelPerk

Retrieves an invoice PDF from TravelPerk.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:invoiceSerialNumber/pdf`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [Get Invoice PDF](https://developers.perk.com/docs/rest-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceSerialNumber` | path | `string` | yes | The invoice serial number whose PDF you want to download. |
