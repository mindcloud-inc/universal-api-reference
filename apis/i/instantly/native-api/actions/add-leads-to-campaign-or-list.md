# Add Leads To Campaign Or List with Instantly

Adds leads to a campaign or list in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/add`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Add Leads To Campaign Or List](https://developer.instantly.ai/api-reference/lead/add-leads-in-bulk-to-a-campaign-or-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leads[]` | body | `array<object>` | yes | Array of lead objects to add. |
| `list_id` | body | `string` | yes | List ID to add leads to. Use this or campaign ID, not both. |
