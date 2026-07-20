# Bulk Assign Leads with Instantly

Assigns leads to users in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/bulk-assign`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Bulk Assign Leads](https://developer.instantly.ai/api-reference/lead/bulk-assign-leads-to-organization-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_user_ids[]` | body | `array<string>` | yes | Organization user IDs to assign matching leads to. |
| `ids[]` | body | `array<string>` | no | Lead IDs to assign. |
