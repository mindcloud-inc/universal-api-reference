# Get Plagiarism Check Status with PlagiarismCheck.org

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/text/:id`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Get Plagiarism Check Status](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Plagiarism check identifier returned by Submit Plagiarism Check. |
