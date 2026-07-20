# <img src="https://images.mindcloud.co/apps/icons/cogmentocrm-2482-logo-1596779297-4mlxv_1778085721067.png" alt="Cogmento CRM logo" width="28" height="28"> Cogmento CRM: Universal API

Cogmento CRM is a customer relationship management platform for managing contacts, deals, tasks, products, and account templates through the Cogmento API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cogmentoCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cogmento.com/
- **Vendor API docs:** https://docs.cogmento.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST |  |
| [List Deals](actions/list-deals.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [List Tasks](actions/list-tasks.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

