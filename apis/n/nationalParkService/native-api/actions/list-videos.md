# List Videos with National Park Service

Retrieves videos from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/multimedia/videos`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Videos](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
