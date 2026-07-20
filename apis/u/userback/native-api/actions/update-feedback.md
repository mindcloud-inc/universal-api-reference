# Update Feedback with Userback

Updates a Userback feedback item.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/feedback/:id`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Update Feedback](https://docs.userback.io/reference/updatefeedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Feedback ID to update. |
| `feedbackType` | body | `string` | no | Updated feedback type. |
| `title` | body | `string` | no | Updated feedback title. |
| `description` | body | `string` | no | Updated feedback description. |
| `pageUrl` | body | `string` | no | Updated page URL. |
| `isShared` | body | `boolean` | no | Whether the feedback is shared. |
| `allowPublicComment` | body | `boolean` | no | Whether public comments are allowed. |
| `priority` | body | `string` | no | Updated priority. |
| `category` | body | `string` | no | Updated category. |
| `rating` | body | `string` | no | Updated rating. |
| `assigneeId` | body | `number` | no | Updated assignee ID. |
| `dueDate` | body | `date` | no | Updated due date. |
| `notify` | body | `boolean` | no | Whether to notify subscribers about the update. |
