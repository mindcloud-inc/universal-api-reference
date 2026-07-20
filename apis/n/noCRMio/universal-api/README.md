# <img src="https://images.mindcloud.co/apps/icons/images-1_1773426684967.jpeg" alt="noCRM.io logo" width="28" height="28"> noCRM.io: Universal API

Connect noCRM.io to read and manage leads, comments, assignments, metadata, users, teams, and client folders through the noCRM REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/noCRMio/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nocrm.io
- **Vendor API docs:** https://www.nocrm.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Leads](actions/list-leads.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Action History

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Action Histories](actions/list-lead-action-histories.md) | GET | Retrieves lead action histories from noCRM.io. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from noCRM.io. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from noCRM.io. |

### Client Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Folder](actions/create-client-folder.md) | POST | Creates a new client folder in noCRM.io. |
| [Delete Client Folder](actions/delete-client-folder.md) | DELETE | Deletes an existing client folder from noCRM.io. |
| [List Client Folders](actions/list-client-folders.md) | GET | Retrieves client folders from noCRM.io. |
| [Retrieve Client Folder](actions/retrieve-client-folder.md) | GET | Retrieves client folder details from noCRM.io. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Comment](actions/create-lead-comment.md) | POST | Creates a new lead comment in noCRM.io. |
| [Delete Lead Comment](actions/delete-lead-comment.md) | DELETE | Deletes an existing lead comment from noCRM.io. |
| [List Lead Comments](actions/list-lead-comments.md) | GET | Retrieves lead comments from noCRM.io. |
| [Update Lead Comment](actions/update-lead-comment.md) | PUT | Updates an existing lead comment in noCRM.io. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from noCRM.io. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead To Client Folder](actions/add-lead-to-client-folder.md) | PUT | Adds a lead to a client folder in noCRM.io. |
| [Assign Lead](actions/assign-lead.md) | PUT | Assigns a lead in noCRM.io. |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in noCRM.io. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from noCRM.io. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from noCRM.io. |
| [List Unassigned Leads](actions/list-unassigned-leads.md) | GET | Retrieves unassigned leads from noCRM.io. |
| [Retrieve Lead](actions/retrieve-lead.md) | GET | Retrieves lead details from noCRM.io. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in noCRM.io. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from noCRM.io. |

### Step

| Action | Method | Description |
| --- | --- | --- |
| [List Steps](actions/list-steps.md) | GET | Retrieves steps from noCRM.io. |
| [Retrieve Step](actions/retrieve-step.md) | GET | Retrieves step details from noCRM.io. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Predefined Tags](actions/list-predefined-tags.md) | GET | Retrieves predefined tags from noCRM.io. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from noCRM.io. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves user details from noCRM.io. |

