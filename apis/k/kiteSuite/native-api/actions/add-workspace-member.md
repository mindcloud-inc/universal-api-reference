# Add Workspace Member with KiteSuite

Adds a member to a workspace in KiteSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspace/member`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Add Workspace Member](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `members[]` | body | `array<string>` | yes | Email addresses to invite to the workspace. Pass an array of emails. Send multiple values as a array. |
| `role` | body | `string` | yes | Workspace role ID to assign. |
