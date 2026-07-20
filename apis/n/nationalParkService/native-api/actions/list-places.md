# List Places with National Park Service

Retrieves places from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/places`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Places](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
