# Get Documents with Alto

Finds documents in Alto by linked record or media type.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Documents](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkedId` | query | `string` | no | Linked record identifier for document lookup. |
| `linkedType` | query | `string` | no | Linked record type for document lookup. |
