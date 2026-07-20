# List Client Properties with Wasi

Retrieves properties linked to a client in Wasi.

## Endpoint

- **Method:** `GET`
- **Path:** `/client/properties/:id_client`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [List Client Properties](https://api.wasi.co/docs/en/guide/clients.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_client` | path | `number` | yes | Wasi client ID whose related properties should be listed. |
