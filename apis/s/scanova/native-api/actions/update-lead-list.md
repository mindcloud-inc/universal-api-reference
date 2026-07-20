# Update Lead List with Scanova

## Endpoint

- **Method:** `PATCH`
- **Path:** `/lead/{lead_list_id}/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Update Lead List](https://docs.scanova.io/api-reference/endpoint/lead_list/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_list_id` | path | `string` | yes | Lead list ID (lead_id) |
| `name` | body | `string` | no | Name of the lead list |
| `is_active` | body | `boolean` | no | Whether to activate or deactivate the lead list |
