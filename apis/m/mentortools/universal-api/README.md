# <img src="https://images.mindcloud.co/apps/icons/mentortools_1774011801823.png" alt="Mentortools logo" width="28" height="28"> Mentortools: Universal API

Review and update Mentortools courses, modules, lessons, and assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mentortools/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mentortools.com/
- **Vendor API docs:** https://app.mentortools.com/public_api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Courses](actions/list-courses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-courses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Patch Course Module Lesson Attached Files](actions/patch-course-module-lesson-attached-files.md) | PUT | Updates lesson attached files in Mentortools, creating new ones when needed. |

### Content Block

| Action | Method | Description |
| --- | --- | --- |
| [List Course Module Lesson Content Blocks](actions/list-course-module-lesson-content-blocks.md) | GET | Retrieves lesson content blocks from Mentortools. |
| [Patch Course Module Lesson Content Blocks](actions/patch-course-module-lesson-content-blocks.md) | PUT | Updates lesson content blocks in Mentortools, creating new ones when needed. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Get Course](actions/get-course.md) | GET | Retrieves a course from Mentortools. |
| [Get Course Info](actions/get-course-info.md) | GET | Retrieves detailed course information from Mentortools. |
| [List Courses](actions/list-courses.md) | GET | Retrieves a list of courses from Mentortools. |
| [Patch Course](actions/patch-course.md) | PUT | Updates part of an existing course in Mentortools. |
| [Update Course](actions/update-course.md) | PUT | Updates an existing course in Mentortools. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Mentortools. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Mentortools. |

### Lesson

| Action | Method | Description |
| --- | --- | --- |
| [Get Course Module Lesson](actions/get-course-module-lesson.md) | GET | Retrieves a course module lesson from Mentortools. |
| [Get Course Module Lesson Info](actions/get-course-module-lesson-info.md) | GET | Retrieves detailed course module lesson information from Mentortools. |
| [List Course Module Lessons](actions/list-course-module-lessons.md) | GET | Retrieves lessons for a course module in Mentortools. |
| [Patch Course Module Lesson](actions/patch-course-module-lesson.md) | PUT | Updates part of an existing course module lesson in Mentortools. |
| [Update Course Module Lesson](actions/update-course-module-lesson.md) | PUT | Updates an existing course module lesson in Mentortools. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Course Module](actions/get-course-module.md) | GET | Retrieves a course module from Mentortools. |
| [Get Course Module Info](actions/get-course-module-info.md) | GET | Retrieves detailed course module information from Mentortools. |
| [List Course Modules](actions/list-course-modules.md) | GET | Retrieves modules for a course in Mentortools. |
| [Patch Course Module](actions/patch-course-module.md) | PUT | Updates part of an existing course module in Mentortools. |
| [Update Course Module](actions/update-course-module.md) | PUT | Updates an existing course module in Mentortools. |

### Submodule

| Action | Method | Description |
| --- | --- | --- |
| [Get Submodule](actions/get-submodule.md) | GET | Retrieves a course submodule from Mentortools. |
| [List Module Submodules](actions/list-module-submodules.md) | GET | Retrieves submodules for a course module in Mentortools. |
| [Patch Module Submodule](actions/patch-module-submodule.md) | PUT | Updates part of an existing submodule in Mentortools. |
| [Update Module Submodule](actions/update-module-submodule.md) | PUT | Updates an existing submodule in Mentortools. |

