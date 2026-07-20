# Create Authorization with Conveyor

Creates an authorization in Conveyor from email or request.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/exchange/authorizations`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Create Authorization](https://docs.conveyor.com/reference/post-authorization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email to authorize when not using a request id. |
| `request_id` | query | `string` | no | Authorization request id to approve. |
| `access_group_ids[]` | query | `array<string>` | no | Access group identifiers for the authorization. |
| `nda_bypass` | query | `boolean` | no | Whether to bypass NDA for the authorization. |
| `expires_at` | query | `date` | no | Authorization expiration date. |
