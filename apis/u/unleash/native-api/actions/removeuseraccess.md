# Remove Project Access For A User with Unleash

Removes project access for a user from Unleash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/admin/projects/{projectId}/users/{userId}/roles`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Remove Project Access For A User](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `userId` | path | `string` | yes | Required path parameter. |
