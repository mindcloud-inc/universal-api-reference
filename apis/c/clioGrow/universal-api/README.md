# <img src="https://images.mindcloud.co/apps/icons/clio-grow-icon-filled-256_1782762061813.png" alt="Clio Grow logo" width="28" height="28"> Clio Grow: Universal API

Clio Grow is Clio's legal intake and CRM API for contacts, inbox leads, matters, notes, users, and custom intake workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clioGrow/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clio.com/grow/
- **Vendor API docs:** https://docs.developers.clio.com/clio-grow/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Contact Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST |  |
| [List Contact Notes](actions/list-contact-notes.md) | GET |  |

### Custom Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Action](actions/create-custom-action.md) | POST |  |
| [List Custom Actions](actions/list-custom-actions.md) | GET |  |

### Inbox Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Lead](actions/create-inbox-lead.md) | POST |  |
| [Get Inbox Lead](actions/get-inbox-lead.md) | GET |  |
| [List Inbox Leads](actions/list-inbox-leads.md) | GET |  |

### Matter

| Action | Method | Description |
| --- | --- | --- |
| [Get Matter](actions/get-matter.md) | GET |  |
| [List Matters](actions/list-matters.md) | GET |  |

### Matter Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Matter Note](actions/create-matter-note.md) | POST |  |
| [List Matter Notes](actions/list-matter-notes.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

