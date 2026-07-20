# Delete Organization Check with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/org/text/delete/:id/`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Delete Organization Check](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Organization plagiarism check identifier. |
| `group_token` | body | `string` | yes | Organization group token required for organization plagiarism checks. |
