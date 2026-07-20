# List Peeps for Vybit with Vybit

## Endpoint

- **Method:** `GET`
- **Path:** `/peeps/{{vybitKey}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [List Peeps for Vybit](https://developer.vybit.net/api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of peep records to return. |
| `offset` | query | `number` | no | Number of peep records to skip. |
| `search` | query | `string` | no | Search peeps by name or email. |
| `vybitKey` | path | `string` | yes | The unique key of the owned vybit whose peeps to list. |
