# Add Project Member with KiteSuite

Adds a member to a project in KiteSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/project/member`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Add Project Member](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectID` | body | `string` | yes | Project ID. |
| `members[]` | body | `array<string>` | yes | Email addresses to add to the project. Pass an array of emails. Send multiple values as a array. |
| `roleID` | body | `string` | yes | Project role ID to assign. |
