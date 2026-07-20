# <img src="https://images.mindcloud.co/apps/icons/trainer-central_1774363120429.png" alt="TrainerCentral logo" width="28" height="28"> TrainerCentral: Universal API

Create courses, host workshops, and manage learners with TrainerCentral

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trainerCentral/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.trainercentral.com
- **Vendor API docs:** https://help.trainercentral.com/portal/en/kb/trainercentral/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Courses](actions/list-courses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-courses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Create Course](actions/create-course.md) | POST | Creates a new course in TrainerCentral. |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from TrainerCentral. |

### Courseattendee

| Action | Method | Description |
| --- | --- | --- |
| [Invite Learner to Course](actions/invite-learner-to-course.md) | POST | Invites a learner to a course in TrainerCentral. |

### Coursemember

| Action | Method | Description |
| --- | --- | --- |
| [List Course Members](actions/list-course-members.md) | GET | Retrieves course members from TrainerCentral. |

### Learner

| Action | Method | Description |
| --- | --- | --- |
| [List Academy Learners](actions/list-academy-learners.md) | GET | Retrieves academy learners from TrainerCentral. |

### Learnerinfo

| Action | Method | Description |
| --- | --- | --- |
| [Get Learner Info](actions/get-learner-info.md) | GET | Retrieves learner info from signup forms in TrainerCentral. |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Portals](actions/list-organization-portals.md) | GET | Retrieves organization portals from TrainerCentral. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Create Chapter](actions/create-chapter.md) | POST | Creates a new chapter in TrainerCentral. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Lesson](actions/create-lesson.md) | POST | Creates a lesson in TrainerCentral. |
| [Create Live Lesson](actions/create-live-lesson.md) | POST | Creates a live lesson in TrainerCentral. |
| [Create Live Workshop](actions/create-live-workshop.md) | POST | Creates a live workshop in TrainerCentral. |
| [List Upcoming Sessions](actions/list-upcoming-sessions.md) | GET | Retrieves upcoming live workshops from TrainerCentral. |

