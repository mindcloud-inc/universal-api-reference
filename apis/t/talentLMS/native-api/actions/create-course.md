# Create Course with TalentLMS

Creates a new course in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Create Course](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-course)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Course name. |
| `code` | body | `string` | no | Course code. |
| `description` | body | `string` | no | Course description. |
| `category_id` | body | `number` | no | Course category ID. |
| `price` | body | `number` | no | Course price. |
| `capacity` | body | `number` | no | Course capacity. |
| `level` | body | `number` | no | Course level. |
| `time_limit` | body | `number` | no | Course time limit. |
| `start_datetime` | body | `string` | no | Course start datetime. |
| `expiration_datetime` | body | `string` | no | Course expiration datetime. |
| `is_active` | body | `boolean` | no | Whether the course is active. |
| `custom_fields` | body | `object` | no | Custom fields object. |
