# List Skills with Dungeon Fighter Online

Retrieves a job's skills from Dungeon Fighter Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/skills/:jobId`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [List Skills](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Dungeon Fighter job ID. |
| `jobGrowId` | query | `string` | yes | Optional job growth ID for filtering the skill list. |
