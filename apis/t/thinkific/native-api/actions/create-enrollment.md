# Create Enrollment with Thinkific

Creates a new enrollment in Thinkific.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrollments`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Create Enrollment](https://developers.thinkific.com/api/api-documentation#/paths/~1enrollments/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activated_at` | body | `date` | no | Enrollment activation timestamp. |
| `course_id` | body | `number` | yes | Course to enroll the user in. |
| `expiry_date` | body | `date` | no | Enrollment expiry date. |
| `user_id` | body | `number` | yes | User to enroll. |
