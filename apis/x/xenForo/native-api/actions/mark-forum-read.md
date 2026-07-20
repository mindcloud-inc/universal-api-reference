# Mark Forum Read with XenForo

Marks a forum as read in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/forums/:id/mark-read`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Mark Forum Read](https://docs.xenforo.com/api/post-forums-id-mark-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the forum to mark read. |
| `date` | body | `number` | no | Unix timestamp to mark the forum read to. Defaults to current time when omitted. |
