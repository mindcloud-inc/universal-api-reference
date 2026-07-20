# Mentortools: Native API Reference

A consolidated summary of Mentortools's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.mentortools.com/public_api/docs
- **OpenAPI specification:** https://app.mentortools.com/public_api/specification/?permission_filter=courses_read&permission_filter=courses_update&permission_filter=mediastorage_create
- **API base URL:** `https://app.mentortools.com/public_api`

## Authentication

### API Key

Use a Mentortools API key generated in the AI Interface.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.mentortools.com/articles/2137977-payment-providers-connecting-mentortools-with-zapier)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 15). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /mediastorage/v1/folders` | [docs](https://app.mentortools.com/public_api/docs) |
| [Get Course](actions/get-course.md) | `GET /courses/v1/:course_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Get Course Info](actions/get-course-info.md) | `GET /courses/v1/:course_id/info` | [docs](https://app.mentortools.com/public_api/docs) |
| [Get Course Module](actions/get-course-module.md) | `GET /courses/v1/modules/:module_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Get Course Module Info](actions/get-course-module-info.md) | `GET /courses/v1/modules/:module_id/info` | [docs](https://app.mentortools.com/public_api/docs) |
| [Get Course Module Lesson](actions/get-course-module-lesson.md) | `GET /courses/v1/lessons/:lesson_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Get Course Module Lesson Info](actions/get-course-module-lesson-info.md) | `GET /courses/v1/lessons/:lesson_id/info` | [docs](https://app.mentortools.com/public_api/docs) |
| [Get Submodule](actions/get-submodule.md) | `GET /courses/v1/submodules/:submodule_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [List Course Module Lesson Content Blocks](actions/list-course-module-lesson-content-blocks.md) | `GET /courses/v1/lessons/:lesson_id/content_blocks` | [docs](https://app.mentortools.com/public_api/docs) |
| [List Course Module Lessons](actions/list-course-module-lessons.md) | `GET /courses/v1/modules/:module_id/lessons` | [docs](https://app.mentortools.com/public_api/docs) |
| [List Course Modules](actions/list-course-modules.md) | `GET /courses/v1/:course_id/modules` | [docs](https://app.mentortools.com/public_api/docs) |
| [List Courses](actions/list-courses.md) | `GET /courses/v1/` | [docs](https://app.mentortools.com/public_api/docs) |
| [List Module Submodules](actions/list-module-submodules.md) | `GET /courses/v1/modules/:module_id/submodules` | [docs](https://app.mentortools.com/public_api/docs) |
| [Patch Course](actions/patch-course.md) | `PATCH /courses/v1/:course_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Patch Course Module](actions/patch-course-module.md) | `PATCH /courses/v1/modules/:module_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Patch Course Module Lesson](actions/patch-course-module-lesson.md) | `PATCH /courses/v1/lessons/:lesson_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Patch Course Module Lesson Attached Files](actions/patch-course-module-lesson-attached-files.md) | `PATCH /courses/v1/lessons/:lesson_id/attached_files` | [docs](https://app.mentortools.com/public_api/docs) |
| [Patch Course Module Lesson Content Blocks](actions/patch-course-module-lesson-content-blocks.md) | `PATCH /courses/v1/lessons/:lesson_id/content_blocks` | [docs](https://app.mentortools.com/public_api/docs) |
| [Patch Module Submodule](actions/patch-module-submodule.md) | `PATCH /courses/v1/submodules/:submodule_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Update Course](actions/update-course.md) | `PUT /courses/v1/:course_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Update Course Module](actions/update-course-module.md) | `PUT /courses/v1/modules/:module_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Update Course Module Lesson](actions/update-course-module-lesson.md) | `PUT /courses/v1/lessons/:lesson_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Update Module Submodule](actions/update-module-submodule.md) | `PUT /courses/v1/submodules/:submodule_id` | [docs](https://app.mentortools.com/public_api/docs) |
| [Upload File](actions/upload-file.md) | `POST /mediastorage/v1/files/upload` | [docs](https://app.mentortools.com/public_api/docs) |
