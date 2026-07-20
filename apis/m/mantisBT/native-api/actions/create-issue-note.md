# Create Issue Note with MantisBT

Creates a new issue note in MantisBT.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/{issue_id}/notes`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Create Issue Note](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `number` | yes | ID of the issue that will receive the note |
| `text` | body | `string` | yes | Text of the note to add |
