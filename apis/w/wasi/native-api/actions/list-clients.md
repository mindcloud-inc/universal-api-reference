# List Clients with Wasi

Finds clients in Wasi by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/client/search`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [List Clients](https://api.wasi.co/docs/en/guide/clients.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_client_origin` | query | `number` | no | Limit clients by acquisition source. |
| `id_client_status` | query | `number` | no | Limit clients by status. |
| `id_client_type` | query | `number` | no | Limit clients by client type. |
| `id_property` | query | `number` | no | Limit clients to those attached to one property. |
| `id_user` | query | `number` | no | Limit clients by assigned Wasi user. |
| `query` | query | `string` | no | Keyword search for matching clients. |
