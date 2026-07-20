# Create Invoice with Payrexx

Creates an invoice in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Bill/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Create Invoice](https://developers.payrexx.com/reference/create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | body | `string` | yes | Invoice language ISO 639-1 code. |
| `currency` | body | `string` | yes | Invoice currency ISO 4217 code. |
| `dueAfterDays` | body | `number` | yes | Allowed invoice due period in days. |
| `recipientCompany` | body | `string` | yes | Recipient company name. |
| `recipientEmail` | body | `string` | yes | Recipient email address. |
| `recipientAddress` | body | `string` | yes | Recipient street address. |
| `recipientZip` | body | `string` | yes | Recipient postal code. |
| `recipientCity` | body | `string` | yes | Recipient city. |
| `recipientCountry` | body | `string` | yes | Recipient country code (ISO 3166-1 alpha-2). |
| `positionTitle` | body | `string` | yes | Invoice line item title. |
| `positionPrice` | body | `number` | yes | Invoice line item price in the smallest currency unit. |
| `positionType` | body | `string` | yes | Invoice line item type. |
| `positionNumber` | body | `number` | yes | Invoice line item quantity/number. |
| `positionVat` | body | `number` | yes | Invoice line item VAT percentage. |
