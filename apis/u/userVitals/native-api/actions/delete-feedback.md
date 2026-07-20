# Delete Feedback with UserVitals

Deletes a feedback item from the roadmap API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/feedback/:publicItemTokenId`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Delete Feedback](https://api.roadmap.space/#delete-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicItemTokenId` | path | `string` | yes | The Base64-encoded public item token id. |
