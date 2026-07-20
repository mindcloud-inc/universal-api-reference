# Create Volume with E2B

Creates a new team volume in E2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/volumes`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Create Volume](https://e2b.dev/docs/api-reference/volumes/post-volumes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the volume. May contain letters, numbers, underscores, and hyphens. |
