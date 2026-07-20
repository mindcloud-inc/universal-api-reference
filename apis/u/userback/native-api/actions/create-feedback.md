# Create Feedback with Userback

Creates a new feedback item in Userback.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Create Feedback](https://docs.userback.io/reference/createfeedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `number` | yes | Feedback project ID. |
| `feedbackType` | body | `string` | yes | Feedback type value. |
| `title` | body | `string` | yes | Feedback title. |
| `description` | body | `string` | no | Feedback description. |
| `email` | body | `string` | no | Feedback submitter email. |
| `name` | body | `string` | no | Feedback submitter name. |
| `pageUrl` | body | `string` | no | Page URL for the feedback. |
| `isShared` | body | `boolean` | no | Whether the feedback is shared. |
| `allowPublicComment` | body | `boolean` | no | Whether public comments are allowed. |
| `priority` | body | `string` | no | Feedback priority. |
| `category` | body | `string` | no | Feedback category. |
| `rating` | body | `string` | no | Feedback rating. |
| `assigneeId` | body | `number` | no | Assignee member ID. |
| `dueDate` | body | `date` | no | Due date for the feedback. |
| `notify` | body | `boolean` | no | Whether to send notifications. |
