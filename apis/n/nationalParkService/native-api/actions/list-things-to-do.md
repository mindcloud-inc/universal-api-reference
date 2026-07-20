# List Things To Do with National Park Service

Retrieves things to do from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/thingstodo`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Things To Do](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | NPS park code. |
| `q` | query | `string` | no | Search term. |
| `stateCode` | query | `string` | no | Two-letter state code. |
