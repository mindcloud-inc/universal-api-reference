# Assign Space Member with Qlik

Assigns a user or group to a space in Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/spaces/:spaceId/assignments`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Assign Space Member](https://qlik.dev/apis/rest/spaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Qlik space ID. |
| `type` | body | `string` | yes | Assignment assignee type, such as user or group. |
| `roles[]` | body | `array<string>` | yes | Roles to grant in the space assignment. |
| `assigneeId` | body | `string` | yes | User or group ID to assign to the space. |
