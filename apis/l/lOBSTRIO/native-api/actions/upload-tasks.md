# Upload Tasks with LOBSTR.IO

Uploads tasks to LOBSTR.IO from a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tasks/upload`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Upload Tasks](https://docs.lobstr.io/docs/upload-tasks)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The CSV or TSV file containing task data. |
| `squid` | body | `string` | yes | The squid hash ID to add tasks to. |
