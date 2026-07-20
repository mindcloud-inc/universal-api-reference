# Store Image To Google Cloud Storage with TinyPNG

Stores a TinyPNG image in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Store Image To Google Cloud Storage](https://tinify.com/developers/reference/http#saving-to-google-cloud-storage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
| `store.gcp_access_token` | body | `string` | yes | Short-lived Google Cloud access token generated from a service account. |
| `store.path` | body | `string` | yes | Destination path in the format <bucket>/<path>/<filename>. |
| `store.headers.Cache-Control` | body | `string` | no | Optional Cache-Control header value to apply on the stored object. |
