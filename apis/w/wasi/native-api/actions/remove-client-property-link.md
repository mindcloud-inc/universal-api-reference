# Remove Client Property Link with Wasi

Deletes a client-to-property relationship from Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/client/:id_client/remove-property/:id_property`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Remove Client Property Link](https://api.wasi.co/docs/en/guide/clients.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_client` | path | `number` | yes | Wasi client ID. |
| `id_property` | path | `number` | yes | Wasi property ID. |
