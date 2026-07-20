# Update Client Property Link with Wasi

Updates a client-to-property relationship in Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/client/:id_client/update-property/:id_property`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Update Client Property Link](https://api.wasi.co/docs/en/guide/clients.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_client` | path | `number` | yes | Wasi client ID. |
| `id_client_type` | query | `number` | yes | Updated relationship client type ID. |
| `id_property` | path | `number` | yes | Wasi property ID. |
