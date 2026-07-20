# Remove Uploaded File with iLoveSign

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://:server/v1/upload/:task/:server_filename`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Remove Uploaded File](https://www.iloveapi.com/docs/api-reference#upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Task-assigned host returned by the start call. |
| `task` | path | `string` | yes | Task identifier that owns the uploaded file. |
| `server_filename` | path | `string` | yes | Uploaded server filename to remove from the task. |
