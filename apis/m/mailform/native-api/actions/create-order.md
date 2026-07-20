# Create Order with Mailform

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://www.mailform.io/app/api/v1`
- **Official documentation:** [Create Order](https://www.mailform.io/docs/api/#create-order)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | PDF document to mail. Use this, Url, or Template as the document source. |
| `url` | body | `string` | no | URL of the PDF document to mail. Ignored if File is provided. |
| `template` | body | `string` | no | Mailform template identifier to use as the document source. |
| `variables` | body | `object` | no | JSON object of template variables. Used only when Template is provided. |
| `customer_reference` | body | `string` | no | Optional customer reference to attach to the order. |
| `service` | body | `list<string>` | yes | Delivery service to use for the order. Accepted values: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `webhook` | body | `string` | no | Webhook URL for order update notifications. |
| `company` | body | `string` | no | Company ID to associate with the order. |
| `simplex` | body | `boolean` | no | Print one page per sheet when true; allow duplex when false. |
| `color` | body | `boolean` | no | Print in color when true; black and white when false. |
| `flat` | body | `boolean` | no | Require mailing in a flat envelope when true. |
| `stamp` | body | `boolean` | no | Require a real postage stamp when true. |
| `return_envelope` | body | `boolean` | no | Include a return envelope when true. |
| `message` | body | `string` | no | Message for postcard or notecard services. |
| `qrcode` | body | `string` | no | QR code to print on supported USPS postcard and first-class mail. |
| `to.name` | body | `string` | yes | Name of the recipient. |
| `to.organization` | body | `string` | no | Organization or company associated with the recipient. |
| `to.address1` | body | `string` | yes | Street number and name of the recipient. |
| `to.address2` | body | `string` | no | Suite, room, or secondary address for the recipient. |
| `to.city` | body | `string` | yes | City of the recipient address. |
| `to.state` | body | `string` | yes | State of the recipient address. |
| `to.postcode` | body | `string` | yes | Postal or ZIP code of the recipient address. |
| `to.country` | body | `string` | yes | Country of the recipient address. |
| `from.name` | body | `string` | yes | Name of the sender. |
| `from.organization` | body | `string` | no | Organization or company associated with the sender. |
| `from.address1` | body | `string` | yes | Street number and name of the sender. |
| `from.address2` | body | `string` | no | Suite, room, or secondary address for the sender. |
| `from.city` | body | `string` | yes | City of the sender address. |
| `from.state` | body | `string` | yes | State of the sender address. |
| `from.postcode` | body | `string` | yes | Postal or ZIP code of the sender address. |
| `from.country` | body | `string` | yes | Country of the sender address. |
