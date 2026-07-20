# Mark Alert with XenForo

Updates an alert's read or viewed status in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/alerts/:id/mark`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Mark Alert](https://docs.xenforo.com/api/post-alerts-id-mark)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the alert to mark. |
| `read` | body | `boolean` | no | If true, marks the alert as read. |
| `unread` | body | `boolean` | no | If true, marks the alert as unread. |
| `viewed` | body | `boolean` | no | If true, marks the alert as viewed. |
