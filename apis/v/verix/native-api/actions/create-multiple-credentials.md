# Create Multiple Credentials with Verix

Creates multiple credentials in Verix for a group.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/credentials/groups/:group_id/`
- **Base URL:** `https://api.verix.io`
- **Official documentation:** [Create Multiple Credentials](https://docs.verix.io/verifiable_credentials_apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `number` | yes | Target Verix group ID for credential creation. |
| `issue` | body | `boolean` | no | When true, issue created credentials immediately. |
| `distribute` | body | `boolean` | no | When true, distribute credentials immediately after issue. |
| `inputs[]` | body | `array<object>` | yes | Array of recipient, credential, custom, and subject payload objects to create. |
