# Get Rate with Mailform

## Endpoint

- **Method:** `POST`
- **Path:** `/rates`
- **Base URL:** `https://www.mailform.io/app/api/v1`
- **Official documentation:** [Get Rate](https://www.mailform.io/docs/api/#get-rate)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | PDF document to price. Use this or Url as the document source. |
| `url` | body | `string` | yes | URL of the PDF document to price. |
| `customer_reference` | body | `string` | no | Optional customer reference for the potential order. |
| `service` | body | `list<string>` | yes | Delivery service to price. Accepted values: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `webhook` | body | `string` | no | Webhook URL for order update notifications if the priced order is later created. |
| `simplex` | body | `boolean` | no | Price one page per sheet when true; allow duplex when false. |
| `color` | body | `boolean` | no | Price color printing when true; black and white when false. |
| `flat` | body | `boolean` | no | Price a flat envelope when true. |
| `stamp` | body | `boolean` | no | Price a real postage stamp when true. |
| `to.name` | body | `string` | yes | Name of the recipient. |
| `to.address1` | body | `string` | yes | Street number and name of the recipient. |
| `to.city` | body | `string` | yes | City of the recipient address. |
| `to.state` | body | `string` | yes | State of the recipient address. |
| `to.postcode` | body | `string` | yes | Postal or ZIP code of the recipient address. |
| `to.country` | body | `string` | yes | Country of the recipient address. |
| `from.name` | body | `string` | yes | Name of the sender. |
| `from.address1` | body | `string` | yes | Street number and name of the sender. |
| `from.city` | body | `string` | yes | City of the sender address. |
| `from.state` | body | `string` | yes | State of the sender address. |
| `from.postcode` | body | `string` | yes | Postal or ZIP code of the sender address. |
| `from.country` | body | `string` | yes | Country of the sender address. |
