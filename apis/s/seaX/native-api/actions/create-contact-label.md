# Create Contact Label with SeaX

Creates a contact label in the current SeaX workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_labels`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Create Contact Label](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact label name. |
