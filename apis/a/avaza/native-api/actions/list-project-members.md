# List Project Members with Avaza

Retrieves project members from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ProjectMember`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Project Members](https://api.avaza.com/#!/ProjectMember/ProjectMember_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectID` | query | `number` | no | Get Project members filtered by ProjectID |
| `UserID` | query | `number` | no | Get Project members filtered by UserID |
