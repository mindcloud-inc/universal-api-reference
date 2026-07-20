# Create Return Shipping Method with Webshipper

Creates a return shipping method in Webshipper.

## Endpoint

- **Method:** `POST`
- **Path:** `/return_shipping_methods`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Create Return Shipping Method](https://docs.webshipper.io/#return_shipping_methods)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | Name of the return shipping method. |
| `data.relationships.portal.data.id` | body | `string` | yes | Return portal ID. |
| `data.relationships.shipping_rate.data.id` | body | `string` | yes | Shipping rate ID. |
