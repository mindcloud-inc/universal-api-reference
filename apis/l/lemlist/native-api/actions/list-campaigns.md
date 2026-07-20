# List Campaigns with lemlist

Retrieves your campaign list from lemlist.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [List Campaigns](https://developer.lemlist.com/api-reference/endpoints/campaigns/get-many-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Filter campaigns by status. Accepted values: `archived`, `draft`, `out_of_credits`, `paused`, `running`. |
