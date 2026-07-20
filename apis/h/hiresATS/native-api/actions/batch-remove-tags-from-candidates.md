# Batch Remove Tags From Candidates with 100Hires ATS

Removes tags from multiple candidates in 100Hires ATS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/candidates/batch/tags`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Batch Remove Tags From Candidates](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Candidate IDs to untag, up to 100 per request. |
| `tags[]` | body | `array<string>` | yes | Tag names to remove from all listed candidates. |
