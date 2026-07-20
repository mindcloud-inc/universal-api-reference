# Enroll User to Course with TalentLMS

Enrolls a user in a course in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrollments`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Enroll User to Course](https://documenter.getpostman.com/view/31867199/2sAY548Kou#enroll-user-to-course)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | body | `number` | yes | Numeric course ID. |
| `user_id` | body | `number` | yes | Numeric user ID. |
