# List Websites with GetResponse

Retrieves a list of websites from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/websites`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Websites](https://apireference.getresponse.com/#operation/getWebsitesList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[name]` | query | `string` | no | Filter websites by name |
| `query[status]` | query | `string` | no | Filter websites by status |
| `stats[from]` | query | `string` | no | Filter website statistics start date |
| `stats[to]` | query | `string` | no | Filter website statistics end date |
| `sort[name]` | query | `string` | no | Sort websites by name |
| `sort[createdAt]` | query | `string` | no | Sort websites by creation date |
| `sort[updatedAt]` | query | `string` | no | Sort websites by update date |
| `sort[pageViews]` | query | `string` | no | Sort websites by page views |
| `sort[visits]` | query | `string` | no | Sort websites by visits |
| `sort[uniqueVisitors]` | query | `string` | no | Sort websites by unique visitors |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
