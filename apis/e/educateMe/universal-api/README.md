# <img src="https://images.mindcloud.co/apps/icons/idh-ociit5o-logos_1774986139812.png" alt="EducateMe logo" width="28" height="28"> EducateMe: Universal API

Create courses, train learners, and track learning progress

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/educateMe/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.educate-me.co/
- **Vendor API docs:** https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in EducateMe. |
| [Delete Activity](actions/delete-activity.md) | DELETE | Deletes an existing activity from EducateMe. |
| [List Course Activities](actions/list-course-activities.md) | GET | Lists course activities in EducateMe. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in EducateMe. |

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Learners' Assignments by Course](actions/list-learners-assignments-by-course.md) | GET | Lists learner assignments for a course in EducateMe. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Create Course](actions/create-course.md) | POST | Creates a new course in EducateMe. |
| [Delete Course](actions/delete-course.md) | DELETE | Deletes an existing course from EducateMe. |
| [List Courses](actions/list-courses.md) | GET | Lists courses in EducateMe. |

### Feedback Note

| Action | Method | Description |
| --- | --- | --- |
| [Export Feedback Notes](actions/export-feedback-notes.md) | GET | Exports feedback notes from EducateMe. |

### Feedback Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Export Feedback Reactions](actions/export-feedback-reactions.md) | GET | Exports feedback reactions from EducateMe. |

### Learner

| Action | Method | Description |
| --- | --- | --- |
| [Delete Learner from Workspace](actions/delete-learner-from-workspace.md) | DELETE | Deletes an existing learner from EducateMe. |
| [Update Learner Suspension Status](actions/update-learner-suspension-status.md) | PUT | Updates a learner's suspension status in EducateMe. |

### Learner Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Invite Learner to Course](actions/invite-learner-to-course.md) | POST | Invites a learner to a course in EducateMe. |
| [Invite Learner to Many Courses](actions/invite-learner-to-many-courses.md) | POST | Invites a learner to multiple courses in EducateMe. |
| [Remove Learner from Course](actions/remove-learner-from-course.md) | DELETE | Removes a learner from a course in EducateMe. |

### Learner Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Learner Session](actions/create-learner-session.md) | POST | Creates a learner session in EducateMe. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Course Schedules](actions/list-course-schedules.md) | GET | Lists course schedules in EducateMe. |
| [Schedule Event Activities for Course](actions/schedule-event-activities-for-course.md) | POST | Schedules event activities for a course in EducateMe. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Learner Submissions](actions/list-learner-submissions.md) | GET | Lists learner submissions for a course in EducateMe. |
| [Submit Assignment for Learner](actions/submit-assignment-for-learner.md) | POST | Submits an assignment for a learner in EducateMe. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in EducateMe. |
| [List Tags](actions/list-tags.md) | GET | Lists tags in EducateMe. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [List Course Transcripts](actions/list-course-transcripts.md) | GET | Lists course transcripts in EducateMe. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Lists users in EducateMe. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in EducateMe. |

