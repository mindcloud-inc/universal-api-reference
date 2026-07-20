# List Webcams with National Park Service

Retrieves webcams from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/webcams`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Webcams](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | NPS webcam identifier. |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
