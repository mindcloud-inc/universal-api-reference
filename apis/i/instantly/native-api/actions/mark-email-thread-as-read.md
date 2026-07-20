# Mark Email Thread As Read with Instantly

Marks an email thread as read in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/emails/threads/:thread_id/mark-as-read`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Mark Email Thread As Read](https://developer.instantly.ai/api/v2/email/markallemailsinathreadasread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `thread_id` | path | `string` | yes | Email thread ID. |
