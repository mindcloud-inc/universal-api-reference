# Update Enrollment with Thinkific

Updates an existing enrollment in Thinkific.

## Endpoint

- **Method:** `PUT`
- **Path:** `/enrollments/:id`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Update Enrollment](https://developers.thinkific.com/api/api-documentation#/paths/~1enrollments~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activated_at` | body | `date` | no | Updated activation timestamp. |
| `expiry_date` | body | `date` | no | Updated expiry date. |
| `id` | path | `number` | yes | Enrollment identifier. |
