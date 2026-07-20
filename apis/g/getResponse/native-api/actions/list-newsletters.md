# List Newsletters with GetResponse

Retrieves a list of newsletters from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/newsletters`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Newsletters](https://apireference.getresponse.com/#operation/getNewsletterList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[subject]` | query | `string` | no | Filter newsletters by subject |
| `query[name]` | query | `string` | no | Filter newsletters by name |
| `query[status]` | query | `string` | no | Filter newsletters by status |
| `query[type]` | query | `string` | no | Filter newsletters by type |
| `query[campaignId]` | query | `string` | no | Filter newsletters by campaign |
| `query[createdOn][from]` | query | `string` | no | Return newsletters created on or after this date |
| `query[createdOn][to]` | query | `string` | no | Return newsletters created on or before this date |
| `query[sendOn][from]` | query | `string` | no | Return newsletters scheduled on or after this date |
| `query[sendOn][to]` | query | `string` | no | Return newsletters scheduled on or before this date |
| `sort[createdOn]` | query | `string` | no | Sort newsletters by creation date |
| `sort[sendOn]` | query | `string` | no | Sort newsletters by send date |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
