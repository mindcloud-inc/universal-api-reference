# Submit AI Check From Text with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chat-gpt/`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Submit AI Check From Text](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Plain text content to scan with the TraceGPT AI detector. |
