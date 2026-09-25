# Update Group with Microsoft Entra

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:groupId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Update Group](https://learn.microsoft.com/en-us/graph/api/group-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `list<string>` | yes | — |
| `displayName` | body | `string` | no | Maximum length: 256. |
| `description` | body | `string` | no | — |
