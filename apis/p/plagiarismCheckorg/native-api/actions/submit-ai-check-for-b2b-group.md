# Submit AI Check For B2B Group with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/chat-gpt/`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Submit AI Check For B2B Group](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Plain text content to scan with the TraceGPT AI detector for a specific B2B group. |
| `group_id` | body | `number` | yes | B2B group identifier documented by the provider for grouped AI checks. |
