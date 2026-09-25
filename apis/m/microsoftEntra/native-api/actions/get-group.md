# Get Group with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:groupId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Get Group](https://learn.microsoft.com/en-us/graph/api/group-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$select` | query | `string` | no |
| `groupId` | path | `list<string>` | yes |
| `$expand` | query | `string` | no |
