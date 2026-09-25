# Remove Group Member with Microsoft Entra

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:groupId/members/:memberId/$ref`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Remove Group Member](https://learn.microsoft.com/en-us/graph/api/group-delete-members?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `list<string>` | yes | — |
| `memberId` | path | `string` | yes | Directory object ID of the member to remove. The object itself is preserved. |
