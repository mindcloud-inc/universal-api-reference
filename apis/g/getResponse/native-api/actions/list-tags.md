# List Tags with GetResponse

Retrieves a list of tags from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Tags](https://apireference.getresponse.com/#operation/getTagsList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[name]` | query | `string` | no | Filter tags by name |
| `query[createdAt][from]` | query | `string` | no | Return tags created on or after this date |
| `query[createdAt][to]` | query | `string` | no | Return tags created on or before this date |
| `sort[createdAt]` | query | `string` | no | Sort tags by creation date |
| `sort[name]` | query | `string` | no | Sort tags by name |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
