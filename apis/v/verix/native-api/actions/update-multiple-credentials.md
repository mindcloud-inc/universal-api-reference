# Update Multiple Credentials with Verix

Updates multiple credentials in Verix for a group.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/credentials/groups/:group_id/`
- **Base URL:** `https://api.verix.io`
- **Official documentation:** [Update Multiple Credentials](https://docs.verix.io/verifiable_credentials_apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `number` | yes | Target Verix group ID for credential updates. |
| `inputs[]` | body | `array<object>` | yes | Array of credential update payloads. |
