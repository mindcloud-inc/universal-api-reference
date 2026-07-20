# Get Document with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Get Document](https://dev.mendeley.com/methods/#retrieving-a-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the document. |
