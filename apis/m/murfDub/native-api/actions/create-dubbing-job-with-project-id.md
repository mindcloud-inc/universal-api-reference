# Create Dubbing Job With Project ID with Murf Dub

Creates a dubbing job in Murf Dub from a project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/murfdub/jobs/create-with-project-id`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Create Dubbing Job With Project ID](https://murf.ai/api/docs/api-reference/dubbing/jobs/create-with-project-id)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Existing Murf Dub project ID. |
| `file` | body | `file` | no | The media file to upload for dubbing. |
| `file_url` | body | `string` | no | Public URL of the media file to dub. |
| `webhook_url` | body | `string` | no | Webhook URL for job status notifications. |
| `file_name` | body | `string` | no | Reference name for the upload. |
| `priority` | body | `string` | no | Processing priority. |
| `webhook_secret` | body | `string` | no | Secret used to validate webhook calls. |
