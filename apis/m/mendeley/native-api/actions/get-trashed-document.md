# Get Trashed Document with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/trash/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Get Trashed Document](https://dev.mendeley.com/methods/#retrieve-a-trashed-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier (UUID) of the trashed document. |
| `view` | query | `string` | no | Includes core document fields plus additional fields. |
