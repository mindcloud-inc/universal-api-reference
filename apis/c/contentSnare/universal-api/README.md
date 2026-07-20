# <img src="https://images.mindcloud.co/apps/icons/content-snare_1773839959667.png" alt="Content Snare logo" width="28" height="28"> Content Snare: Universal API

Manage requests, clients, team members, templates, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/contentSnare/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://contentsnare.com/
- **Vendor API docs:** https://api.contentsnare.com/partner_api/v1/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Requests](actions/list-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in Content Snare. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes a client from Content Snare. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Content Snare. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Content Snare. |
| [Update Client](actions/update-client.md) | PUT | Updates a client in Content Snare. |

### Client Company

| Action | Method | Description |
| --- | --- | --- |
| [List Client Companies](actions/list-client-companies.md) | GET | Retrieves client companies from Content Snare. |

### Communication Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Communications Schedules](actions/list-communications-schedules.md) | GET | Retrieves communications schedules from Content Snare. |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Current User Data](actions/retrieve-current-user-data.md) | GET | Retrieves current user data from Content Snare. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Content Snare. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Approve All Submitted Page Fields](actions/approve-all-submitted-page-fields.md) | PUT | Approves all submitted fields for a page in Content Snare. |
| [Create Page](actions/create-page.md) | POST | Creates a page in Content Snare. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Content Snare. |
| [Submit All Page Fields For Review](actions/submit-all-page-fields-for-review.md) | PUT | Submits all page fields for review in Content Snare. |

### Page Template

| Action | Method | Description |
| --- | --- | --- |
| [List Page Templates](actions/list-page-templates.md) | GET | Retrieves page templates from Content Snare. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Approve All Submitted Fields](actions/approve-all-submitted-fields.md) | PUT | Approves all submitted fields for a request in Content Snare. |
| [Create Request](actions/create-request.md) | POST | Creates a request in Content Snare. |
| [Delete Request](actions/delete-request.md) | DELETE | Deletes a request from Content Snare. |
| [Get Request](actions/get-request.md) | GET | Retrieves a request from Content Snare. |
| [List Requests](actions/list-requests.md) | GET | Retrieves requests from Content Snare. |
| [Review Request](actions/review-request.md) | PUT | Reviews a request field in Content Snare. |
| [Run Integration Actions](actions/run-integration-actions.md) | PUT | Runs integration actions for a request in Content Snare. |
| [Submit All Fields For Review](actions/submit-all-fields-for-review.md) | PUT | Submits all request fields for review in Content Snare. |
| [Update Request](actions/update-request.md) | PUT | Updates a request in Content Snare. |

### Request Template

| Action | Method | Description |
| --- | --- | --- |
| [List Request Templates](actions/list-request-templates.md) | GET | Retrieves request templates from Content Snare. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Approve All Submitted Section Fields](actions/approve-all-submitted-section-fields.md) | PUT | Approves all submitted fields for a section in Content Snare. |
| [Create Section](actions/create-section.md) | POST | Creates a section in Content Snare. |
| [Submit All Section Fields For Review](actions/submit-all-section-fields-for-review.md) | PUT | Submits all section fields for review in Content Snare. |

### Section Template

| Action | Method | Description |
| --- | --- | --- |
| [List Section Templates](actions/list-section-templates.md) | GET | Retrieves section templates from Content Snare. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Team Member](actions/create-team-member.md) | POST | Creates a team member in Content Snare. |
| [Delete Team Member](actions/delete-team-member.md) | DELETE | Deletes a team member from Content Snare. |
| [Get Team Member](actions/get-team-member.md) | GET | Retrieves a team member from Content Snare. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Content Snare. |
| [Update Team Member](actions/update-team-member.md) | PUT | Updates a team member in Content Snare. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Content Snare. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Content Snare. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Content Snare. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Content Snare. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in Content Snare. |

