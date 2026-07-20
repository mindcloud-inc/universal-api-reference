# Mark Thread as Read with Twist

Marks a Twist thread as read.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/mark_read`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Mark Thread as Read](https://developer.twist.com/v3/#mark-thread-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | The id of the thread. |
| `obj_index` | query | `number` | yes | The index of the last known read message. |
