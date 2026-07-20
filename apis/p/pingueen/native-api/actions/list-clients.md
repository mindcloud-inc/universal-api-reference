# List Clients with Pingueen

## Endpoint

- **Method:** `GET`
- **Path:** `/clients`
- **Base URL:** `https://api.pingueen.it/ext/v2/{businessname}`
- **Official documentation:** [List Clients](https://etinet.gitbook.io/pingueen/api-reference/clients/retrive-a-list-of-clients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | query | `string` | no | Filter clients by client ID. |
| `ds_phone` | query | `string` | no | Filter clients by phone number. |
