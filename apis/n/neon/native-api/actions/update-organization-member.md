# Update role for organization member with Neon

Updates a role for organization member in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organizations/:org_id/members/:member_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update role for organization member](https://api-docs.neon.tech/reference/updateorganizationmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `member_id` | path | `string` | yes | Neon API parameter member_id |
| `role` | body | `list` | yes | Neon API parameter role Accepted values: `0`, `1`. |
