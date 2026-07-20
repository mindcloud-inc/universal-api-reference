# Get BibTeX Document with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Get BibTeX Document](https://dev.mendeley.com/methods/#retrieving-a-bibtex-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/x-bibtex` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the document. |
