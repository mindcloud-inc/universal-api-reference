# Unredeem Student Points with Xperiencify

Unredeems student points in Xperiencify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/redeem_points/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Unredeem Student Points](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_a34840f3e2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_ids[]` | body | `array<number>` | yes | One or more course IDs. |
| `student_ids[]` | body | `array<number>` | yes | One or more student IDs. |
| `points_type` | body | `string` | yes | Use xp, xxp, or bp. |
| `value` | body | `number` | yes | Positive number of points. |
