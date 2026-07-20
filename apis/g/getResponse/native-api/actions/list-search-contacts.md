# List Search Contacts with GetResponse

Retrieves saved search contact lists from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/search-contacts`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Search Contacts](https://apireference.getresponse.com/#operation/getSearchContactsList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[name]` | query | `string` | no | Filter search contacts by name |
| `query[createdOn][from]` | query | `string` | no | Return search contacts created on or after this date |
| `query[createdOn][to]` | query | `string` | no | Return search contacts created on or before this date |
| `sort[name]` | query | `string` | no | Sort search contacts by name |
| `sort[createdOn]` | query | `string` | no | Sort search contacts by creation date |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
