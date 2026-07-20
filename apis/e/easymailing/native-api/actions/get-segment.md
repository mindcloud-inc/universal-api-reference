# Get Segment with Easymailing

Retrieves a segment from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/list_segments/{{uuid}}`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Segment](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `uuid` | path | `string` | yes | Segment UUID. |
