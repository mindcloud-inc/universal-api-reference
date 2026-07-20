# Get Multiple Projects with Scale

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects`
- **Base URL:** `https://api.scale.com`
- **Official documentation:** [Get Multiple Projects](https://docs.genai.scale.com/v2/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only return projects created after this ISO 8601 timestamp. |
| `created_before` | query | `string` | no | Only return projects created before this ISO 8601 timestamp. |
