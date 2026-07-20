# Upload File From URL with iLoveSign

## Endpoint

- **Method:** `POST`
- **Path:** `https://:server/v1/upload`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Upload File From URL](https://www.iloveapi.com/docs/api-reference#upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Task-assigned server host returned by Start Sign Task, for example api11.ilovepdf.com. |
| `task` | body | `string` | yes | Sign task ID returned by Start Sign Task. |
| `cloud_file` | body | `string` | yes | Public URL of the PDF file to upload to the sign task. |
