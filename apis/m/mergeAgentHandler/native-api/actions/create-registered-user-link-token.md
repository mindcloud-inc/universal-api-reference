# Create Registered User Link Token with Merge Agent Handler

Creates a registered user link token in Merge Agent Handler.

## Endpoint

- **Method:** `POST`
- **Path:** `/registered-users/:registered_user_id/link-token/`
- **Base URL:** `https://ah-api.merge.dev/api/v1`
- **Official documentation:** [Create Registered User Link Token](https://docs.merge.dev/merge-agent-handler/agent-handler/link-token/create-for-registered-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registered_user_id` | path | `string` | no | ID of the registered user. |
