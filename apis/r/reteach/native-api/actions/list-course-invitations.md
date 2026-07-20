# List Course Invitations with Reteach

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/course-invitation`
- **Base URL:** `https://api.reteach.io`
- **Official documentation:** [List Course Invitations](https://api.reteach.io/docs/#/CourseInvitation/CourseInvitationController_findMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerIdentifier` | query | `string` | no | Filter by the customer id, email, username, or externalId. |
| `courseId` | query | `string` | no | Filter by the id of the course. |
