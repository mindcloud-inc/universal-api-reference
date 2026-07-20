# Upload File with DomoAI

Creates a new file upload slot in DomoAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/upload/file`
- **Base URL:** `https://api.domoai.com`
- **Official documentation:** [Upload File](https://docs.domoai.app/api-reference/upload/upload-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | The filename DomoAI should use for the upload slot. |
