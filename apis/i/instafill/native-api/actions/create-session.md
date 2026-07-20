# Create Session with Instafill

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sessions`
- **Base URL:** `https://api.instafill.ai`
- **Official documentation:** [Create Session](https://docs.instafill.ai/docs/api/sessions/create-session)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form_id` | body | `string` | no |
| `file_urls` | body | `list<string>` | no |
| `text_info` | body | `string` | no |
| `profile_ids` | body | `list<string>` | no |
| `session_id` | body | `string` | no |
| `is_batch` | body | `boolean` | no |
