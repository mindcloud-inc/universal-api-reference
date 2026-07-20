# Add Followup with Cursor

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/agents/{{id}}/followup`
- **Base URL:** `https://api.cursor.com`
- **Official documentation:** [Add Followup](https://cursor.com/docs/cloud-agent/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for the cloud agent receiving the follow-up. |
| `prompt.text` | body | `string` | yes | Follow-up instruction for the agent. |
| `prompt.images[]` | body | `array<object>` | no | Optional array of base64 encoded images, maximum 5. |
