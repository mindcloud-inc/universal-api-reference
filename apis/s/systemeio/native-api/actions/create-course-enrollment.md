# Create Course Enrollment with Systeme.io

Creates a course enrollment in Systeme.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/school/courses/:courseId/enrollments`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Create Course Enrollment](https://developer.systeme.io/reference/api_schoolcourses_courseidenrollments_post-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | Course identifier. |
| `contactId` | body | `number` | yes | Contact ID to enroll in the course. |
| `accessType` | body | `string` | yes | Enrollment access type: partial_access, full_access, or dripping_content. |
