# Submit Plagiarism Check with PlagiarismCheck.org

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/text`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Submit Plagiarism Check](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Plain text content to check for plagiarism. The official docs require at least 80 characters. |
