# Remove member from the organization with Neon

Removes organization member from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:org_id/members/:member_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Remove member from the organization](https://api-docs.neon.tech/reference/removeorganizationmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `member_id` | path | `string` | yes | Neon API parameter member_id |
