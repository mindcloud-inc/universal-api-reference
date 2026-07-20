# Get Custom Feed with Dealfront

Retrieves a custom feed from Dealfront.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/custom-feeds/:custom_feed_id`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Get Custom Feed](https://docs.leadfeeder.com/api/#get-a-specific-custom-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | ID of the account that owns the custom feed. |
| `custom_feed_id` | path | `string` | yes | ID of the custom feed to retrieve. |
