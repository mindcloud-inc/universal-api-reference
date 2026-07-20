# Metadata Lookup with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/metadata`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Metadata Lookup](https://dev.mendeley.com/methods/#metadata-lookup)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document-lookup.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doi` | query | `string` | no | Digital Object Identifier to match. |
| `title` | query | `string` | no | Title terms to match. |
| `authors` | query | `string` | no | Author names to match. |
