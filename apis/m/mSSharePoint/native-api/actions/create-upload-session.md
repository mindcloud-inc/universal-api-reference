# Create Upload Session with MS SharePoint

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/drives/:driveId/items/:parentItemId:/:fileName:/createUploadSession`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Upload Session](https://learn.microsoft.com/en-us/graph/api/driveitem-createuploadsession?view=graph-rest-1.0#example-1-create-an-upload-session)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | — |
| `parentItemId` | path | `string` | yes | The destination folder ID. Use root for the drive root folder. |
| `fileName` | path | `string` | yes | — |
| `item` | body | `object` | no | — |
| `item.conflictBehavior` | body | `list<string>` | no | Accepted values: `fail`, `rename`, `replace`. |
| `item.name` | body | `string` | no | If supplied, must match File Name. |
| `deferCommit` | body | `boolean` | no | Requires a separate completion request after all bytes are uploaded when enabled. |
