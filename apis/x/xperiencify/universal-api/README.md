# <img src="https://images.mindcloud.co/apps/icons/xperiencify_1773840224669.png" alt="Xperiencify logo" width="28" height="28"> Xperiencify: Universal API

Manage courses, students, tags, and reward points

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xperiencify/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xperiencify.com
- **Vendor API docs:** https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Courses](actions/list-courses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Course

| Action | Method | Description |
| --- | --- | --- |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from Xperiencify. |

### Student

| Action | Method | Description |
| --- | --- | --- |
| [Add Student to Course](actions/add-student-to-course.md) | POST | Creates a student enrollment in an Xperiencify course. |
| [Get Student Info](actions/get-student-info.md) | GET | Retrieves student details from Xperiencify by email address. |
| [List Students](actions/list-students.md) | GET | Retrieves students from Xperiencify with an optional course filter. |
| [Remove Student From All Courses](actions/remove-student-from-all-courses.md) | DELETE | Deletes a student from all Xperiencify courses. |
| [Remove Student From Course](actions/remove-student-from-course.md) | DELETE | Deletes a student's enrollment from an Xperiencify course. |
| [Update Basic Student Info](actions/update-basic-student-info.md) | PUT | Updates a student's basic information in Xperiencify. |
| [Update Student Custom Field](actions/update-student-custom-field.md) | PUT | Updates a student custom field in Xperiencify. |

### Student Points

| Action | Method | Description |
| --- | --- | --- |
| [Redeem Student Points](actions/redeem-student-points.md) | PUT | Redeems student points in Xperiencify. |
| [Unredeem Student Points](actions/unredeem-student-points.md) | PUT | Unredeems student points in Xperiencify. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add New Tag](actions/add-new-tag.md) | POST | Creates new tags in Xperiencify. |
| [Add Tags to Student](actions/add-tags-to-student.md) | PUT | Updates a student's tags in Xperiencify. |
| [List Student Tags](actions/list-student-tags.md) | GET | Retrieves tags for a student in Xperiencify. |
| [Remove Tag](actions/remove-tag.md) | DELETE | Deletes tags from Xperiencify. |
| [Remove Tags from Student](actions/remove-tags-from-student.md) | DELETE | Deletes tags from a student in Xperiencify. |

