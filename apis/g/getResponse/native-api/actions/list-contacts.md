# List Contacts with GetResponse

Retrieves a list of contacts from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Contacts](https://apireference.getresponse.com/#operation/getContactList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[email]` | query | `string` | no | Filter contacts by email |
| `query[name]` | query | `string` | no | Filter contacts by name |
| `query[campaignId]` | query | `string` | no | Filter contacts by campaign |
| `query[origin]` | query | `string` | no | Filter contacts by origin |
| `query[createdOn][from]` | query | `string` | no | Return contacts created on or after this date |
| `query[createdOn][to]` | query | `string` | no | Return contacts created on or before this date |
| `query[changedOn][from]` | query | `string` | no | Return contacts changed on or after this date |
| `query[changedOn][to]` | query | `string` | no | Return contacts changed on or before this date |
| `sort[email]` | query | `string` | no | Sort by email order |
| `sort[name]` | query | `string` | no | Sort by name order |
| `sort[createdOn]` | query | `string` | no | Sort by creation date order |
| `sort[changedOn]` | query | `string` | no | Sort by change date order |
| `sort[campaignId]` | query | `string` | no | Sort by campaign ID order |
| `additionalFlags` | query | `string` | no | Additional behavior flags (for example exactMatch) |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
