# Create Contact with SeaX

Creates a contact in the current SeaX workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Create Contact](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact name. |
