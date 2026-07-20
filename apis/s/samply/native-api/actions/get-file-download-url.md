# Get File Download URL with Samply

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectid/files/:fileid/download`
- **Base URL:** `https://samply.app/api/v0`
- **Official documentation:** [Get File Download URL](https://docs.samply.app/api/files.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileid` | path | `string` | no | The Samply file, folder, or stack id. |
| `projectid` | path | `string` | no | The Samply project id. |
