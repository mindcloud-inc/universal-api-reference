# Upload Object with Google Cloud Storage

Uploads an object to Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload/storage/v1/b/:bucket/o`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Upload Object](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | path | `list<string>` | yes | Bucket to upload into. |
| `name` | query | `string` | yes | Name to give the uploaded object. |
| `file` | body | `file` | yes | File content to upload. |
