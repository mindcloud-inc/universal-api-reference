# Submit Organization File Check with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/org/text/check/`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Submit Organization File Check](https://plagiarismcheck.org/for-developers/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_token` | body | `string` | yes | Organization group token required for organization plagiarism checks. |
| `author` | body | `string` | yes | Email of the organization member who will own the check. |
| `file` | body | `file` | yes | Document file to check within the organization account. |
