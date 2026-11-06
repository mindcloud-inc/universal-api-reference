# Share File with Microsoft Teams

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/drives/:driveId/items/:fileId/invite`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Share File](https://learn.microsoft.com/en-us/graph/api/driveitem-invite?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Use parentReference.driveId returned by Upload Chat File. |
| `fileId` | path | `string` | yes | Use id returned by Upload Chat File. |
| `recipients[]` | body | `array<object>` | yes | All intended recipients from List Chat Members. Each recipient must have an email address. Grants read access without sending invitation emails. |
| `recipients[].email` | body | `string` | yes | Use email from List Chat Members. Do not send the chat message until access has been confirmed for every intended recipient. |
