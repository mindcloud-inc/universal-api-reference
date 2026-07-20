# List Forms with Typeform

## Endpoint

- **Method:** `GET`
- **Path:** `/forms`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [List Forms](https://www.typeform.com/developers/create/reference/retrieve-forms/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Filter forms by text. |
| `workspace_id` | query | `list` | no | Limit forms to one workspace. |
