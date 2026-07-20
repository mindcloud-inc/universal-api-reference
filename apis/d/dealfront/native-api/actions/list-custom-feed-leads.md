# List Custom Feed Leads with Dealfront

Retrieves leads for a custom feed in Dealfront.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/custom-feeds/:custom_feed_id/leads`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [List Custom Feed Leads](https://docs.leadfeeder.com/api/#get-leads-for-custom-feed)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | ID of the account whose custom feed leads you want to list. |
| `custom_feed_id` | path | `string` | yes | ID of the custom feed whose leads you want to list. |
| `start_date` | query | `string` | yes | Start date for the lead search window in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the lead search window in YYYY-MM-DD format. |
