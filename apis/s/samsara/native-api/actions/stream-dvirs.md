# Stream DVIRs with Samsara

## Endpoint

- **Method:** `GET`
- **Path:** `dvirs/stream`
- **Base URL:** `https://api.samsara.com/`
- **Official documentation:** [Stream DVIRs](https://developers.samsara.com/reference/getdvirs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startTime` | query | `string` | yes | DVIR stream start in RFC 3339 format. |
| `endTime` | query | `string` | no | DVIR stream end in RFC 3339 format. |
