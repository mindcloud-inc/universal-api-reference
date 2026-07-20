# Get Organization Check Status with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/org/text/status/:id/`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Get Organization Check Status](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Organization plagiarism check identifier. |
| `group_token` | body | `string` | yes | Organization group token required for organization plagiarism checks. |
