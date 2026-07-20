# <img src="https://images.mindcloud.co/apps/icons/streak_1773236115335.png" alt="Streak logo" width="28" height="28"> Streak: Universal API

Manage sales pipelines and customer relationships in Gmail

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/streak/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.streak.com
- **Vendor API docs:** https://streak.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Box

| Action | Method | Description |
| --- | --- | --- |
| [Create Box](actions/create-box.md) | POST | Creates a new box in Streak. |
| [Get Box](actions/get-box.md) | GET | Retrieves a box from Streak. |
| [Get multiple boxes](actions/get-multiple-boxes.md) | GET | Retrieves multiple boxes from a Streak pipeline. |
| [List Pipeline Boxes](actions/list-pipeline-boxes.md) | GET | Retrieves boxes from a Streak pipeline. |
| [Update Box](actions/update-box.md) | PUT | Updates an existing box in Streak. |

### Box Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Boxes By Name](actions/search-boxes-by-name.md) | GET | Finds boxes in Streak by exact name. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Streak. |
| [List Box Comments](actions/list-box-comments.md) | GET | Retrieves comments for a box in Streak. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Streak. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Streak. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Streak. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get or Create Organization](actions/get-or-create-organization.md) | POST | Finds an organization in Streak, or creates one if needed. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Streak. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Streak. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a pipeline from Streak. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Streak. |

### Pipeline Field

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Fields](actions/list-pipeline-fields.md) | GET | Retrieves pipeline fields from Streak. |

### Pipeline Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | GET | Retrieves pipeline stages from Streak. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Boxes, Contacts, and Organizations](actions/search-boxes-contacts-and-organizations.md) | GET | Finds boxes, contacts, and organizations in Streak by query. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Streak. |
| [List Box Tasks](actions/list-box-tasks.md) | GET | Retrieves tasks for a box in Streak. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Streak. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [List Box Threads](actions/list-box-threads.md) | GET | Retrieves threads for a box in Streak. |

### Timeline Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Box Timeline](actions/get-box-timeline.md) | GET | Retrieves timeline entries for a box in Streak. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Streak. |

