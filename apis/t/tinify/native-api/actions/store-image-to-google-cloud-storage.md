# Store Image To Google Cloud Storage with Tinify

Stores an optimized image from Tinify in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/output/:outputId`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Store Image To Google Cloud Storage](https://tinify.com/developers/reference/http#saving-to-google-cloud-storage)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | Tinify output identifier from a prior compression URL. |
| `store.gcp_access_token` | body | `string` | yes | Google Cloud access token with permission to write to the target bucket path. |
| `store.path` | body | `string` | yes | Destination path in the format bucket/path/filename. |
