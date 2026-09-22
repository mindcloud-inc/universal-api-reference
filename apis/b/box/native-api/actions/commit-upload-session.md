# Commit Upload Session with Box

## Endpoint

- **Method:** `POST`
- **URL:** `https://upload.box.com/api/2.0/files/upload_sessions/:session_id/commit`
- **Official documentation:** [Commit Upload Session](https://developer.box.com/reference/post-files-upload-sessions-id-commit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | Upload session ID returned by Create Upload Session. |
| `wholeFileSha1` | body | `string` | yes | The complete file in base64, the same value the parts were sliced from. Box needs a checksum of the whole file to close the upload and this action works it out for you. A 40-character hexadecimal SHA-1 is also accepted if you already have one. |
| `parts` | body | `array<object>` | yes | List of part objects returned by Upload Part, ordered by offset. |
