# Update Course with Mentortools

Updates an existing course in Mentortools.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/v1/:course_id`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [Update Course](https://app.mentortools.com/public_api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `number` | yes | The course ID. |
| `title` | body | `string` | yes | Title of the course. |
| `order` | body | `number` | yes | Order of the course in the list. |
| `is_active` | body | `boolean` | yes | Whether the course is active and available for users. |
| `is_secret` | body | `boolean` | yes | Whether the course is secret. |
| `is_archived` | body | `boolean` | yes | Whether the course is archived. |
| `is_displayed_in_app` | body | `boolean` | yes | Whether the course is displayed in mobile app. |
| `is_offline_downloadable` | body | `boolean` | yes | Whether the course can be downloaded for offline access. |
