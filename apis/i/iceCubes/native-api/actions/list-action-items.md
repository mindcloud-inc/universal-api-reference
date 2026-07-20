# List Action Items with IceCubes

## Endpoint

- **Method:** `GET`
- **Path:** `/action-items`
- **Base URL:** `https://icecubes.app/api/public`
- **Official documentation:** [List Action Items](https://icecubes.app/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_id` | query | `string` | no | Filter action items by meeting ID. |
| `completed` | query | `boolean` | no | Filter by completion status. |
| `tag` | query | `string` | no | Filter by tag name. |
