# List Sessions with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/sessions`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [List Sessions](https://docs.umami.is/docs/api/sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | no | Start timestamp in milliseconds. |
| `startAt` | query | `number` | yes | Timestamp in milliseconds for the start of the reporting range. |
| `endAt` | query | `number` | no | End timestamp in milliseconds. |
| `endAt` | query | `number` | yes | Timestamp in milliseconds for the end of the reporting range. |
| `search` | query | `string` | no | Optional search text. |
