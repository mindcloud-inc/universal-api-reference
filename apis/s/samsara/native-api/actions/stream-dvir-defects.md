# Stream DVIR Defects with Samsara

## Endpoint

- **Method:** `GET`
- **Path:** `defects/stream`
- **Base URL:** `https://api.samsara.com/`
- **Official documentation:** [Stream DVIR Defects](https://developers.samsara.com/reference/streamdefects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startTime` | query | `string` | yes | Defect stream start in RFC 3339 format. |
| `endTime` | query | `string` | no | Defect stream end in RFC 3339 format. |
