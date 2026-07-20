# Unlink Feedback with UserVitals

Unlinks feedback from a parent idea or story.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/feedback/:publicItemTokenId/unlink/:parentId`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Unlink Feedback](https://api.roadmap.space/#unlink-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentId` | path | `string` | yes | The parent idea or story id. |
| `publicItemTokenId` | path | `string` | yes | The Base64-encoded public item token id. |
