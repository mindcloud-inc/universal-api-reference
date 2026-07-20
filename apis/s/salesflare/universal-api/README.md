# <img src="https://images.mindcloud.co/apps/icons/images-4_1774032332450.png" alt="Salesflare logo" width="28" height="28"> Salesflare: Universal API

Salesflare is a B2B CRM platform for managing accounts, contacts, opportunities, tasks, and related sales activity.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesflare/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salesflare.com
- **Vendor API docs:** https://api.salesflare.com/docs#section/Introduction/Authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [Delete Account](actions/delete-account.md) | DELETE |  |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST |  |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE |  |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |
| [Update Opportunity](actions/update-opportunity.md) | PUT |  |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET |  |

### Stage

| Action | Method | Description |
| --- | --- | --- |
| [Get Stage](actions/get-stage.md) | GET |  |
| [List Stages](actions/list-stages.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

