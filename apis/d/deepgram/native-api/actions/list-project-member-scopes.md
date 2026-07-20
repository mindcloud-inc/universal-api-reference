# List Project Member Scopes with Deepgram

Retrieves project member scopes from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/members/:member_id/scopes`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [List Project Member Scopes](https://developers.deepgram.com/reference/manage/members/scopes/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Deepgram project identifier to inspect. |
| `member_id` | path | `string` | yes | The Deepgram member identifier to inspect. |
