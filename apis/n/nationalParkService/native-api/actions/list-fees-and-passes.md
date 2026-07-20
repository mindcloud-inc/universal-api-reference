# List Fees And Passes with National Park Service

Retrieves fees and passes from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/feespasses`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Fees And Passes](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | Comma-delimited NPS park codes. |
| `q` | query | `string` | no | Search term. |
| `statecode` | query | `string` | no | Comma-delimited two-letter state codes. |
