# List Audio with National Park Service

Retrieves audio resources from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/multimedia/audio`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Audio](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
| `stateCode` | query | `string` | no | Comma-delimited two-letter state codes. |
