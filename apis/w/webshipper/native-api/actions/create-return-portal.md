# Create Return Portal with Webshipper

Creates a return portal in Webshipper.

## Endpoint

- **Method:** `POST`
- **Path:** `/return_portals`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Create Return Portal](https://docs.webshipper.io/#return_portals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | Name of the return portal. |
| `data.relationships.order_channel.data.id` | body | `string` | yes | The order channel ID to connect to the portal. |
| `data.relationships.slip_template.data.id` | body | `string` | no | Optional slip template ID. |
| `data.relationships.mail_template.data.id` | body | `string` | no | Optional mail template ID. |
| `data.relationships.return_address.data.id` | body | `string` | no | Optional return address ID. |
