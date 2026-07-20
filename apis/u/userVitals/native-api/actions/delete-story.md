# Delete Story with UserVitals

Deletes a story from the roadmap API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/stories/:publicItemTokenId`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Delete Story](https://api.roadmap.space/#delete-story)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicItemTokenId` | path | `string` | yes | The Base64-encoded public item token id. |
