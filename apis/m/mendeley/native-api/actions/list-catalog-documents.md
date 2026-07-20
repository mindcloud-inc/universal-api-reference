# List Catalog Documents with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [List Catalog Documents](https://dev.mendeley.com/methods/#retrieving-catalog-documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doi` | query | `string` | yes | Digital Object Identifier. |
| `view` | query | `string` | no | Includes core document fields plus additional fields. |
