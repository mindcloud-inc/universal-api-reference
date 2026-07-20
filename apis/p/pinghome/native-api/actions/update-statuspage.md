# Update Statuspage with Pinghome

Updates an existing statuspage in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/statuspage-cmd/v1/statuspage/:id`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Statuspage](https://docs.pinghome.io/statuspages/update-statuspage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Statuspage ID to update. |
| `subscription_enabled` | body | `boolean` | no | Whether public statuspage subscriptions are enabled. |
| `name` | body | `string` | yes | Updated statuspage name. |
| `description` | body | `string` | yes | Updated statuspage description. |
| `subdomain` | body | `string` | yes | Updated subdomain. |
| `type` | body | `string` | yes | Updated statuspage type. |
