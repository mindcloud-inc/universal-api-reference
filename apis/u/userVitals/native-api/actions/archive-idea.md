# Archive Idea with UserVitals

Archives an idea in the roadmap API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ideas/:publicItemTokenId`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Archive Idea](https://api.roadmap.space/#archive-idea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicItemTokenId` | path | `string` | yes | The Base64-encoded public item token id. |
