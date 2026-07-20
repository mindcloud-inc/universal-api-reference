# Link Client To Property with Wasi

Creates a client-to-property relationship in Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/client/:id_client/add-property/:id_property`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Link Client To Property](https://api.wasi.co/docs/en/guide/clients.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_client` | path | `number` | yes | Wasi client ID. |
| `id_client_type` | query | `number` | yes | Relationship client type ID. |
| `id_property` | path | `number` | yes | Wasi property ID. |
