# <img src="https://images.mindcloud.co/apps/icons/poodll_1775761148813.png" alt="Poodll logo" width="28" height="28"> Poodll: Universal API

Manage Moodle users, enrollments, groups, cohorts, and site info

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/poodll/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://poodll.com
- **Vendor API docs:** https://support.poodll.com/support/solutions/19000105053

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site Info](actions/get-site-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-site-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Cohortmembership

| Action | Method | Description |
| --- | --- | --- |
| [Add Cohort Members](actions/add-cohort-members.md) | POST | Adds members to a cohort in Poodll. |
| [Remove Cohort Members](actions/remove-cohort-members.md) | DELETE | Removes members from a cohort in Poodll. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [Get Courses](actions/get-courses.md) | GET | Retrieves course records from Poodll. |
| [Get Courses By Field](actions/get-courses-by-field.md) | GET | Finds courses in Poodll by a specific field. |

### Customaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Actions](actions/get-custom-actions.md) | GET | Retrieves available custom actions from Poodll. |

### Customactionfield

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Action Details](actions/get-custom-action-details.md) | GET | Retrieves custom action field details from Poodll. |

### Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Enrol Users](actions/enrol-users.md) | POST | Enrols users in a Poodll course. |
| [Get Enrolled Users](actions/get-enrolled-users.md) | GET | Retrieves enrolled users from a Poodll course. |
| [Unenrol Users](actions/unenrol-users.md) | DELETE | Unenrols users from a Poodll course. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Course Groups](actions/get-course-groups.md) | GET | Retrieves groups from a Poodll course. |

### Groupmembership

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Members](actions/add-group-members.md) | POST | Adds members to a group in Poodll. |
| [Remove Group Members](actions/remove-group-members.md) | DELETE | Removes members from a group in Poodll. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Info](actions/get-site-info.md) | GET | Retrieves site information and services from Poodll. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create Users](actions/create-users.md) | POST | Creates new user accounts in Poodll. |
| [Delete Users](actions/delete-users.md) | DELETE | Deletes existing user accounts from Poodll. |
| [Get Users By Field](actions/get-users-by-field.md) | GET | Finds users in Poodll by a specific field. |
| [Search Users](actions/search-users.md) | GET | Finds users in Poodll by search criteria. |
| [Update Users](actions/update-users.md) | PUT | Updates existing user accounts in Poodll. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Deregister Webhook](actions/deregister-webhook.md) | DELETE | Deregisters a webhook for an event in Poodll. |
| [Register Webhook](actions/register-webhook.md) | POST | Registers a webhook for an event in Poodll. |

### Webhooksample

| Action | Method | Description |
| --- | --- | --- |
| [Sample Webhook](actions/sample-webhook.md) | GET | Retrieves a sample webhook payload from Poodll. |

