# List Activations with KEYZY

Retrieves activations for a KEYZY license serial number.

## Endpoint

- **Method:** `GET`
- **Path:** `/activations/:serial`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [List Activations](https://www.keyzy.io/docs/developers/rest-api/activations-get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serial` | path | `string` | yes | A license serial number. |
