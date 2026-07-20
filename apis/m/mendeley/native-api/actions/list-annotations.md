# List Annotations with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/annotations`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [List Annotations](https://dev.mendeley.com/methods/#retrieving-annotations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-annotation.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | query | `string` | no | Filter annotations by document. |
