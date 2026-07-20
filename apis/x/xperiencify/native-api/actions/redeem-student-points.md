# Redeem Student Points with Xperiencify

Redeems student points in Xperiencify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/redeem_points/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Redeem Student Points](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_cf0b8a7c4a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_ids[]` | body | `array<number>` | yes | One or more course IDs. |
| `student_ids[]` | body | `array<number>` | yes | One or more student IDs. |
| `points_type` | body | `string` | yes | Use xp, xxp, or bp. |
| `value` | body | `number` | yes | Positive number of points. |
