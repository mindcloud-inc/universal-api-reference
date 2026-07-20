# Request Chat Export with Pachca (Admin)

Requests a chat export from the Pachca Admin API.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/exports`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Request Chat Export](https://dev.pachca.com/api/common/request-export)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_at` | body | `date` | yes |
| `end_at` | body | `date` | yes |
| `webhook_url` | body | `string` | yes |
| `chat_ids[]` | body | `array<number>` | no |
| `skip_chats_file` | body | `boolean` | no |
