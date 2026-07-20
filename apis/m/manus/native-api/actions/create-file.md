# Create File with Manus

Creates a file in Manus and returns a presigned upload URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://api.manus.ai/v1`
- **Official documentation:** [Create File](https://open.manus.ai/docs/v1/create-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Name of the file to upload |
