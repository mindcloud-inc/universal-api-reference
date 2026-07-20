# Update Space Assignment with Qlik

Updates an existing space assignment in Qlik.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/spaces/:spaceId/assignments/:assignmentId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Update Space Assignment](https://qlik.dev/apis/rest/spaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Qlik space ID. |
| `assignmentId` | path | `string` | yes | Qlik space assignment ID. |
| `roles[]` | body | `array<string>` | yes | Replacement roles for the assignment. |
