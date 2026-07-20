# Create Order with Print.one Postcards

Creates a new order in Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/orders`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Create Order](https://api.print.one/docs/v2#operation/Order/createOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | Template ID for the order |
| `finish` | body | `string` | yes | Finish of the postcard |
| `mergeVariables` | body | `object` | yes | Personalization data as a JSON object |
| `recipient.name` | body | `string` | yes | Recipient name |
| `recipient.address` | body | `string` | yes | Recipient street address |
| `recipient.postalCode` | body | `string` | yes | Recipient postal code |
| `recipient.city` | body | `string` | yes | Recipient city |
| `recipient.country` | body | `string` | yes | Recipient country ISO code |
