# List Visitor Centers with National Park Service

Retrieves visitor centers from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/visitorcenters`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Visitor Centers](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
| `q` | query | `string` | no | Search term. |
| `stateCode` | query | `string` | no | Comma-delimited two-letter state codes. |
