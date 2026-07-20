# Validate Plagiarism Text Before Submit with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/text/validate`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Validate Plagiarism Text Before Submit](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Plain text content to validate before submitting a plagiarism check. The official docs require at least 80 characters. |
