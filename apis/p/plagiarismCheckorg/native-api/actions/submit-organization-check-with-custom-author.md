# Submit Organization Check With Custom Author with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/org/text/check/`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Submit Organization Check With Custom Author](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_token` | body | `string` | yes | Organization group token required for organization plagiarism checks. |
| `author` | body | `string` | yes | Email of the organization member who will own the check. |
| `text` | body | `string` | yes | Plain text content to check within the organization account. |
| `custom_author` | body | `string` | yes | Optional display author name when the real author is not registered in the organization account. |
