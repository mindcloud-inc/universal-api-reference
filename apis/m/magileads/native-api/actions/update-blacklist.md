# Update Blacklist with Magileads

Updates an existing blacklist in Magileads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/blacklists/:blacklist_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Update Blacklist](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blacklist_id` | path | `number` | yes | The blacklist ID. |
| `name` | body | `string` | no | The updated blacklist name. |
