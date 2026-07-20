# Create Project Key with Deepgram

Creates a new project API key in Deepgram.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/keys`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Create Project Key](https://developers.deepgram.com/reference/manage/keys/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `scopes` | body | `string` | yes | Scopes to grant to the created project key. |
| `expiration_date` | body | `string` | yes | Expiration timestamp for the created project key in ISO 8601 format. |
| `comment` | body | `string` | no | Human-readable comment stored with the project key. |
