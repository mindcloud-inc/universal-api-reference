# Create Comment with Samply

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectid/files/:fileid/comments`
- **Base URL:** `https://samply.app/api/v0`
- **Official documentation:** [Create Comment](https://docs.samply.app/api/comments.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileid` | path | `string` | no | The Samply file, folder, or stack id. |
| `projectid` | path | `string` | no | The Samply project id. |
