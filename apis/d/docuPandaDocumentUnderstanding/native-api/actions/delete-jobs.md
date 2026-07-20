# Delete Jobs with DocuPanda - Document Understanding

Deletes existing jobs from DocuPanda.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/jobs`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Jobs](https://docs.docupipe.ai/reference/delete_jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobIds` | body | `list<string>` | yes | List of job IDs to be deleted. |
| `jobIds[]` | body | `array<string>` | yes | List of job IDs to be deleted. |
