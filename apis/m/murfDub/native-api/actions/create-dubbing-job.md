# Create Dubbing Job with Murf Dub

Creates a dubbing job in Murf Dub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/murfdub/jobs/create`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Create Dubbing Job](https://murf.ai/api/docs/api-reference/dubbing/jobs/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | The media file to upload for dubbing. |
| `file_url` | body | `string` | no | Public URL of the media file to dub. |
| `source_locale` | body | `string` | no | Source language locale. |
| `target_locales` | body | `string<string>` | yes | Target locale to dub the file into. |
| `webhook_url` | body | `string` | no | Webhook URL for job status notifications. |
| `file_name` | body | `string` | no | Reference name for the upload. |
| `priority` | body | `string` | no | Processing priority. |
| `webhook_secret` | body | `string` | no | Secret used to validate webhook calls. |
