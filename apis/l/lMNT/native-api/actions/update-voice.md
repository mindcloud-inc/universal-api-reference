# Update Voice with LMNT

Updates an existing voice in LMNT.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/ai/voice/:id`
- **Base URL:** `https://api.lmnt.com`
- **Official documentation:** [Update Voice](https://docs.lmnt.com/api-reference/voice/update-voice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional updated description for the voice. |
| `gender` | body | `string` | no | Optional updated gender tag for the voice. |
| `id` | path | `string` | yes | The id of the voice. |
| `name` | body | `string` | no | Optional updated display name for the voice. |
| `starred` | body | `boolean` | no | When true, adds the voice to your starred list. |
