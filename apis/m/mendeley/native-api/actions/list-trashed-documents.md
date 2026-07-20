# List Trashed Documents with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/trash`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [List Trashed Documents](https://dev.mendeley.com/methods/#retrieve-all-trashed-documents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deleted_since` | query | `string` | no | Return only documents deleted since this ISO 8601 timestamp. |
| `group_id` | query | `string` | no | Return trashed documents for the specified group. |
| `modified_since` | query | `string` | no | Return only documents modified since this ISO 8601 timestamp. |
| `order` | query | `string` | no | Sort order. |
| `sort` | query | `string` | no | Field to sort on. |
| `view` | query | `string` | no | Includes core document fields plus additional fields. |
