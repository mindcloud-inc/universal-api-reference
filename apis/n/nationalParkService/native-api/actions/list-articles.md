# List Articles with National Park Service

Retrieves articles from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/articles`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Articles](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
| `q` | query | `string` | no | Search term. |
| `stateCode` | query | `string` | no | Comma-delimited two-letter state codes. |
