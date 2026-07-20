# List Hooks with Grain

Retrieves hooks from Grain.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/hooks`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [List Hooks](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | — |
| `filter.hook_type` | body | `list` | no | Only return hooks with the matching hook type. Accepted values: `highlight_added`, `highlight_deleted`, `highlight_updated`, `recording_added`, `recording_deleted`, `recording_updated`, `story_added`, `story_deleted`, `story_updated`, `upload_status`. |
| `filter.state` | body | `list` | no | Only return hooks that are either enabled or disabled. Accepted values: `disabled`, `enabled`. |
