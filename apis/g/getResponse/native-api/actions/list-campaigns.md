# List Campaigns with GetResponse

Retrieves a list of campaigns from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [List Campaigns](https://apireference.getresponse.com/#operation/getCampaignList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[name]` | query | `string` | no | Filter campaigns by name |
| `query[isDefault]` | query | `string` | no | Filter campaigns by default flag |
| `sort[name]` | query | `string` | no | Sort campaigns by name |
| `sort[createdOn]` | query | `string` | no | Sort campaigns by creation date |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
