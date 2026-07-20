# Get Catalog Document with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Get Catalog Document](https://dev.mendeley.com/methods/#retrieving-a-catalog-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The catalog id (UUID). |
| `view` | query | `string` | no | Includes core document fields plus additional fields. |
