# <img src="https://images.mindcloud.co/apps/icons/gorilla-desk_1773862395103.png" alt="GorillaDesk logo" width="28" height="28"> GorillaDesk: Universal API

Manage customers, users, and service data in GorillaDesk.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gorillaDesk/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gorilladesk.com
- **Vendor API docs:** https://api.gorilladesk.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Company](actions/retrieve-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Company](actions/retrieve-company.md) | GET | Retrieves company details from GorillaDesk. |

### Customer Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Note](actions/create-customer-note.md) | POST | Creates a customer note in GorillaDesk. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in GorillaDesk. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from GorillaDesk. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from GorillaDesk. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in GorillaDesk. |

### Phone Type

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Types](actions/list-phone-types.md) | GET | Retrieves phone types from GorillaDesk. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from GorillaDesk. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from GorillaDesk. |

