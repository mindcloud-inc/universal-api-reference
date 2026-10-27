# Get File Upload URL with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `files.getUploadURLExternal`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Get File Upload URL](https://docs.slack.dev/reference/methods/files.getUploadURLExternal/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `length` | body | `number` | yes | Exact file size in bytes. |
| `filename` | body | `string` | yes | File name sent to Slack. |
