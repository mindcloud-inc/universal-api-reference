# Submit AI Check From File with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chat-gpt/`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Submit AI Check From File](https://plagiarismcheck.org/for-developers/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File to scan with the TraceGPT AI detector. |
