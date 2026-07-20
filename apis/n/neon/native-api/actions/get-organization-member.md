# Retrieve organization member details with Neon

Retrieves organization member details from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org_id/members/:member_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve organization member details](https://api-docs.neon.tech/reference/getorganizationmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `member_id` | path | `string` | yes | Neon API parameter member_id |
