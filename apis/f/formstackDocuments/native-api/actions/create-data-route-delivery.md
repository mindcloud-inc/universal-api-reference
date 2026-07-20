# Create Data Route Delivery with Formstack Documents

Creates a data route delivery in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/routes/:id/deliveries`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Create Data Route Delivery](https://www.webmerge.me/developers/routes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the data route to create a delivery for |
| `settings[from]` | body | `string` | no | Sender address for email deliveries |
| `settings[html]` | body | `string` | no | HTML body for email deliveries |
| `settings[subject]` | body | `string` | no | Subject for email deliveries |
| `settings[to]` | body | `string` | no | Recipient value for email deliveries |
| `type` | body | `string` | yes | Delivery type such as email or webhook |
