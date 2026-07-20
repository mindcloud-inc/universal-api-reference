# Mark Notifications As Read with Unstructured

Marks notifications as read in Unstructured.

## Endpoint

- **Method:** `POST`
- **Path:** `/notifications/mark-read`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Mark Notifications As Read](https://docs.unstructured.io/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notification_ids[]` | body | `array<string>` | no | Notification IDs to mark as read. |
| `before` | body | `string` | no | Mark all notifications before this time as read. |
| `mark_all` | body | `boolean` | no | Mark all notifications as read. |
| `workflow_id` | body | `string` | no | Workflow filter when marking notifications as read. |
