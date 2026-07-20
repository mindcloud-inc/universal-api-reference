# Move Leads with Instantly

Moves leads to a campaign or list in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/move`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Move Leads](https://developer.instantly.ai/api-reference/lead/move-leads-to-a-campaign-or-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Lead IDs to include when moving leads. |
| `list_id` | body | `string` | yes | Source list ID to filter leads from. |
| `to_list_id` | body | `string` | yes | Destination list ID. |
