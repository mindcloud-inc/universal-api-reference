# Get Employee with Paycom

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/employee/:eecode/:sensitive`
- **Base URL:** `https://api.paycomonline.net/v4/rest/index.php/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eecode` | path | `string` | no | — |
| `sensitive` | path | `list` | no | Include sensitive information in the response |
