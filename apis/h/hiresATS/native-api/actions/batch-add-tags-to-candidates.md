# Batch Add Tags To Candidates with 100Hires ATS

Adds tags to multiple candidates in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates/batch/tags`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Batch Add Tags To Candidates](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Candidate IDs to tag, up to 100 per request. |
| `tags[]` | body | `array<string>` | yes | Tag names to add to all listed candidates. |
