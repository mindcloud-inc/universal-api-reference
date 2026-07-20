# List People with National Park Service

Retrieves people from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/people`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List People](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
