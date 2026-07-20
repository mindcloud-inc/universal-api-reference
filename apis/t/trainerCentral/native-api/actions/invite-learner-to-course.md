# Invite Learner to Course with TrainerCentral

Invites a learner to a course in TrainerCentral.

## Endpoint

- **Method:** `POST`
- **Path:** `/addCourseAttendee.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [Invite Learner to Course](https://help.trainercentral.com/portal/en/kb/articles/invite-learner-to-course-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseAttendee.email` | body | `string` | yes | The learner email address to invite. |
| `courseAttendee.firstName` | body | `string` | yes | The learner first name. |
| `courseAttendee.lastName` | body | `string` | yes | The learner last name. |
| `courseAttendee.courseId` | body | `string` | yes | The course ID the learner should be invited to. |
| `courseAttendee.password` | body | `string` | no | Optional learner password. |
| `courseAttendee.expiryTime` | body | `number` | no | Optional course access expiry timestamp in milliseconds. |
