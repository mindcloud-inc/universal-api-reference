# Update Contact with Syncro

Updates an existing contact in Syncro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Update Contact](https://api-docs.syncromsp.com/#/Contact/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Syncro contact ID. |
| `customer_id` | body | `number` | no | — |
| `name` | body | `string` | yes | — |
| `address1` | body | `string` | no | — |
| `address2` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `zip` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `mobile` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
