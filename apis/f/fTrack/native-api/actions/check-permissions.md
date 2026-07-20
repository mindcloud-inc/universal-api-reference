# Check Permissions with FTrack

Checks permissions in FTrack for an entity.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Check Permissions](https://developer.ftrack.com/api/operations/permissions-api-permissions-permissions-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | body | `string` | yes | Entity type whose permissions should be evaluated. |
| `entity_data` | body | `object` | yes | Entity payload used for the permission check. |
| `expression` | body | `string` | no | Optional permission expression to evaluate. |
