# Update Return Shipping Method with Webshipper

Updates a return shipping method in Webshipper.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/return_shipping_methods/:id`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Update Return Shipping Method](https://docs.webshipper.io/#return_shipping_methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The return shipping method ID. |
| `data.id` | body | `string` | yes | Repeat the ID value for the JSON:API request body. |
| `data.attributes.name` | body | `string` | no | Updated return shipping method name. |
