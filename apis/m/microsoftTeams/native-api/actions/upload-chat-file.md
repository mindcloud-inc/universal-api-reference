# Upload Chat File with Microsoft Teams

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.0/me/drive/root:/:fileName:/content`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Upload Chat File](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | path | `string` | yes | File name including extension. Saves in the connected user's OneDrive root. An existing file with the same name is replaced; use a unique name to avoid replacing another file. |
| `content` | body | `file` | yes | Base64 file content or a direct HTTPS download URL. Uploads binary bytes using the Teams connection. Does not share the file or send a message. |
