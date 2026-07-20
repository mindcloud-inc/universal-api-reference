# Create Site with Makeswift

Creates a new site in Makeswift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/sites`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Create Site](https://docs.makeswift.com/developer/reference/api/sites/create-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes | Workspace ID that will own the new site. |
| `name` | body | `string` | yes | Name for the new site. |
