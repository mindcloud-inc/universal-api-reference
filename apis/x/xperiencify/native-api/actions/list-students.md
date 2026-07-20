# List Students with Xperiencify

Retrieves students from Xperiencify with an optional course filter.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/coach/students/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [List Students](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_2562793d8e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | query | `number` | no | Filter students by course. |
