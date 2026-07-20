# Create Course Review with Thinkific

Creates a new course review in Thinkific.

## Endpoint

- **Method:** `POST`
- **Path:** `/course_reviews`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Create Course Review](https://developers.thinkific.com/api/api-documentation#/paths/~1course_reviews/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approved` | body | `boolean` | yes | Whether the review is approved. |
| `course_id` | query | `number` | yes | Course ID for the review. |
| `rating` | body | `number` | yes | Review rating. |
| `review_text` | body | `string` | yes | Review text content. |
| `title` | body | `string` | yes | Review title. |
| `user_id` | body | `number` | yes | ID of the user creating the review. |
