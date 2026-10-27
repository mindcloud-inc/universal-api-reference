# Complete File Upload with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `files.completeUploadExternal`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Complete File Upload](https://docs.slack.dev/reference/methods/files.completeUploadExternal/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<object>` | yes | File IDs from Get File Upload URL, with optional titles. |
| `files[].id` | body | `string` | yes | The file_id returned by Get File Upload URL. |
| `files[].title` | body | `string` | no | Optional display title for this uploaded file. |
| `channel_id` | body | `string` | no | Channel where Slack should share the finalized file. Omit to keep private. |
| `thread_ts` | body | `string` | no | Parent message timestamp when sharing in a thread. |
| `initial_comment` | body | `string` | no | Optional message introducing the file. |
