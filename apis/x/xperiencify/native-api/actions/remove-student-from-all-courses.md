# Remove Student From All Courses with Xperiencify

Deletes a student from all Xperiencify courses.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/course/remove/all/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Remove Student From All Courses](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_67a038c345)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student_email` | body | `string` | yes | Email address for the student. |
