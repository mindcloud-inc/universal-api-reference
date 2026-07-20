# Get Branches with Alto

Retrieves branch records from your Alto account.

## Endpoint

- **Method:** `GET`
- **Path:** `/branches`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Branches](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activeOnly` | query | `boolean` | no | When true, returns only active branches. |
