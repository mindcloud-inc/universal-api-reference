# Create Campaign with SeaX

Creates a campaign in the current SeaX workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Create Campaign](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_service_id` | body | `string` | yes | Messaging service identifier. |
| `mode` | body | `string` | yes | Campaign mode. |
| `name` | body | `string` | yes | Campaign name. |
| `phone_ids` | body | `list<string>` | yes | Phone identifiers to send from. |
| `stage` | body | `string` | yes | Campaign stage. |
| `type` | body | `string` | yes | Campaign type. |
