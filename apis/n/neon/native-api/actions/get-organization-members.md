# Retrieve organization members details with Neon

Retrieves organization members from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org_id/members`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve organization members details](https://api-docs.neon.tech/reference/getorganizationmembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `sort_by` | query | `list` | no | Neon API parameter sort_by Accepted values: `0`, `1`, `2`. |
| `sort_order` | query | `list` | no | Neon API parameter sort_order Accepted values: `0`, `1`. |
