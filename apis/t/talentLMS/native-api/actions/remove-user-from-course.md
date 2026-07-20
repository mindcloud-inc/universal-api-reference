# Remove User from Course with TalentLMS

Removes a user from a course in TalentLMS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/enrollments`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Remove User from Course](https://documenter.getpostman.com/view/31867199/2sAY548Kou#delete-a-user-from-a-course)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `number` | yes | Numeric course ID. |
| `user_id` | body | `number` | yes | Numeric user ID. |
