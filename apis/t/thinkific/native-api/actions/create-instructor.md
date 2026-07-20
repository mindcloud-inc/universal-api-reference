# Create Instructor with Thinkific

Creates a new instructor in Thinkific.

## Endpoint

- **Method:** `POST`
- **Path:** `/instructors`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Create Instructor](https://developers.thinkific.com/api/api-documentation#/paths/~1instructors/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Instructor email address. |
| `first_name` | body | `string` | yes | Instructor first name. |
| `last_name` | body | `string` | yes | Instructor last name. |
| `slug` | body | `string` | yes | Unique instructor slug. |
