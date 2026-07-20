# Get Video Annotations with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/annotations/:id`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Video Annotations](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Video ID to fetch annotations for. |
| `source` | query | `string` | no | Annotation source: archive or youtube. |
