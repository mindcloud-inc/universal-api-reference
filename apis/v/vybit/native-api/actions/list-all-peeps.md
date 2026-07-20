# List All Peeps with Vybit

## Endpoint

- **Method:** `GET`
- **Path:** `/peeps`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [List All Peeps](https://developer.vybit.net/api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of peep records to return. |
| `offset` | query | `number` | no | Number of peep records to skip. |
| `search` | query | `string` | no | Search peeps by name or email. |
