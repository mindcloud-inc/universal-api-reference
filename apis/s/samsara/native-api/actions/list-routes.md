# List Routes with Samsara

## Endpoint

- **Method:** `GET`
- **Path:** `fleet/routes`
- **Base URL:** `https://api.samsara.com/`
- **Official documentation:** [List Routes](https://developers.samsara.com/reference/fetchroutes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startTime` | query | `string` | yes | Route range start in RFC 3339 format. |
| `endTime` | query | `string` | yes | Route range end in RFC 3339 format. |
