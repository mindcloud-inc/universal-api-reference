# List Tours with National Park Service

Retrieves tours from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/tours`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Tours](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
