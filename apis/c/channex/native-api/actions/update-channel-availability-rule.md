# Update Channel Availability Rule with Channex

Updates a channel availability rule in Channex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/channel_availability_rules/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Update Channel Availability Rule](https://docs.channex.io/api-v.1-documentation/availability-rules-collection#update-availability-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the channel availability rule to update. |
| `channel_availability_rule` | body | `object` | yes | Top-level channel_availability_rule payload object documented by Channex for rule updates. |
