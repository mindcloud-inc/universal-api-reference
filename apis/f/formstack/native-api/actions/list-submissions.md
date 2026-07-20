# List Submissions with Formstack

Retrieves submissions across all forms from Formstack.

## Endpoint

- **Method:** `GET`
- **Path:** `/submissions`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [List Submissions](https://developers.formstack.com/reference/getsubmissionslist-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Search term to filter submissions by content. |
| `order` | query | `list<string>` | no | Sort order for results (ASC or DESC). Accepted values: `ASC`, `DESC`. |
