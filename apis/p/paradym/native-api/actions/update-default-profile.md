# Update Default Profile with Paradym

Updates the default project profile in Paradym.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/profiles/default`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Update Default Profile](https://paradym.id/reference#tag/project-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | The display name shown for the default profile. |
