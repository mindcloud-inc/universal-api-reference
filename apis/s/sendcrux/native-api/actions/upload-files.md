# Upload Files with Sendcrux

Uploads one or more files to Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/file/upload`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Upload Files](https://api.sendbound.com/files/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `string` | yes | A JSON array string of files to upload. Each item should contain `url` and optional `subdirectory`. |
