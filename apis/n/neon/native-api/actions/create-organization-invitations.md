# Create organization invitations with Neon

Creates organization invitations in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:org_id/invitations`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create organization invitations](https://api-docs.neon.tech/reference/createorganizationinvitations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `invitations[]` | body | `array<object>` | yes | Neon API parameter invitations |
