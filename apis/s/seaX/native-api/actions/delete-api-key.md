# Delete API Key with SeaX

Deletes an API key from the current SeaX workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api_keys/{api_key_id}`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Delete API Key](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key_id` | path | `string` | yes | API key identifier. |
