# Get Multiple Skills with Dungeon Fighter Online

Retrieves details for multiple skills from Dungeon Fighter Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/multi/skills/:jobId`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Get Multiple Skills](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Dungeon Fighter job ID. |
| `skillIds` | query | `string` | yes | Comma-separated Dungeon Fighter skill IDs. |
