# Xperiencify: Native API Reference

A consolidated summary of Xperiencify's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api
- **API base URL:** `https://api.xperiencify.io`

## Authentication

### API Key

Connect with your Xperiencify API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add New Tag](actions/add-new-tag.md) | `POST /api/public/coach/tag/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_6efc54fbe5) |
| [Add Student to Course](actions/add-student-to-course.md) | `POST /api/public/student/create/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_6ebaea9e33) |
| [Add Tags to Student](actions/add-tags-to-student.md) | `POST /api/public/student/tag/manager/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_287215e459) |
| [Get Student Info](actions/get-student-info.md) | `POST /api/public/student/info/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_acaa21e682) |
| [List Courses](actions/list-courses.md) | `GET /api/public/coach/courses/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_64e0180278) |
| [List Student Tags](actions/list-student-tags.md) | `POST /api/public/student/tag/list/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_ed3982e551) |
| [List Students](actions/list-students.md) | `GET /api/public/coach/students/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_2562793d8e) |
| [Redeem Student Points](actions/redeem-student-points.md) | `POST /api/public/student/redeem_points/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_cf0b8a7c4a) |
| [Remove Student From All Courses](actions/remove-student-from-all-courses.md) | `POST /api/public/student/course/remove/all/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_67a038c345) |
| [Remove Student From Course](actions/remove-student-from-course.md) | `POST /api/public/student/course/remove/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_f8ef3e3a68) |
| [Remove Tag](actions/remove-tag.md) | `DELETE /api/public/coach/tag/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_14c30a3daa) |
| [Remove Tags from Student](actions/remove-tags-from-student.md) | `DELETE /api/public/student/tag/manager/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_4b331bbfab) |
| [Unredeem Student Points](actions/unredeem-student-points.md) | `POST /api/public/student/redeem_points/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_a34840f3e2) |
| [Update Basic Student Info](actions/update-basic-student-info.md) | `PATCH /api/public/student/update/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_e7f1a14bd1) |
| [Update Student Custom Field](actions/update-student-custom-field.md) | `POST /api/public/student/customfield/` | [docs](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_a27eec35e6) |
