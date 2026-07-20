# Create Client with Wasi

Creates a new client in Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/client/add`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Create Client](https://api.wasi.co/docs/en/guide/clients.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | no | Client address. |
| `birthday` | query | `date` | no | Client birthday. |
| `cell_phone` | query | `string` | no | Client mobile phone number. |
| `comment` | query | `string` | no | Client comment. |
| `email` | query | `string` | no | Client email address. |
| `first_name` | query | `string` | no | Client first name. |
| `id_city` | query | `number` | no | Client city ID. |
| `id_client_origin` | query | `number` | no | Client origin ID. |
| `id_client_status` | query | `number` | no | Client status ID. |
| `id_client_type` | query | `number` | no | Primary client type ID. |
| `id_country` | query | `number` | no | Client country ID. |
| `id_region` | query | `number` | no | Client region ID. |
| `id_user` | query | `number` | no | Assigned Wasi user ID. |
| `identification` | query | `string` | no | Client identification number. |
| `last_name` | query | `string` | no | Client last name. |
| `phone` | query | `string` | no | Client phone number. |
| `reference` | query | `string` | no | Client reference. |
| `send_information` | query | `boolean` | no | Whether the client accepts information messages. |
