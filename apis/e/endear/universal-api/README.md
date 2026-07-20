# <img src="https://images.mindcloud.co/apps/icons/images-3_1774362848270.png" alt="Endear logo" width="28" height="28"> Endear: Universal API

Endear is a retail CRM and clienteling platform for customer profiles, conversations, notes, tasks, teams, users, and external customer or catalog sync through its GraphQL Admin API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/endear/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.endearhq.com
- **Vendor API docs:** https://docs.endearhq.com/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Current Integration](actions/current-integration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endear/latest/actions/current-integration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Current Brand](actions/current-brand.md) | GET |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [Search Conversations](actions/search-conversations.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Assign Users To Customer](actions/assign-users-to-customer.md) | PUT |  |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customers By External IDs](actions/get-customers-by-external-ids.md) | GET |  |
| [Search Customers](actions/search-customers.md) | GET |  |
| [Unassign Users From Customer](actions/unassign-users-from-customer.md) | PUT |  |
| [Update Customer](actions/update-customer.md) | PUT |  |
| [Update Customer Field Attributes](actions/update-customer-field-attributes.md) | PUT |  |

### Customer Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Field](actions/create-customer-field.md) | POST |  |
| [Get Customer Fields By IDs](actions/get-customer-fields-by-ids.md) | GET |  |
| [Get Customer Fields By Keys](actions/get-customer-fields-by-keys.md) | GET |  |
| [List Customer Fields](actions/list-customer-fields.md) | GET |  |

### Draft

| Action | Method | Description |
| --- | --- | --- |
| [Get Drafts By IDs](actions/get-drafts-by-ids.md) | GET |  |
| [Search Drafts](actions/search-drafts.md) | GET |  |

### External Customer

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upsert External Customers](actions/bulk-upsert-external-customers.md) | PUT |  |

### External Product

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upsert External Products](actions/bulk-upsert-external-products.md) | PUT |  |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Current Integration](actions/current-integration.md) | GET |  |
| [Get Integration](actions/get-integration.md) | GET |  |
| [List Integrations](actions/list-integrations.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |
| [Search Messages](actions/search-messages.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Get Note](actions/get-note.md) | GET |  |
| [Search Notes](actions/search-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Note Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Note Comment](actions/create-note-comment.md) | POST |  |
| [Update Note Comment](actions/update-note-comment.md) | PUT |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Assign Users To Task](actions/assign-users-to-task.md) | PUT |  |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [Search Tasks](actions/search-tasks.md) | GET |  |
| [Unassign Users From Task](actions/unassign-users-from-task.md) | PUT |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET |  |
| [List Teams](actions/list-teams.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

