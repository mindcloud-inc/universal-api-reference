# <img src="https://images.mindcloud.co/apps/icons/agendor_1773932328033.png" alt="Agendor logo" width="28" height="28"> Agendor: Universal API

Agendor CRM API integration for people, organizations, deals, and account actions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agendor/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.agendor.com.br
- **Vendor API docs:** https://api.agendor.com.br/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agendor/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in Agendor. |
| [Delete Organization](actions/delete-organization.md) | DELETE | Deletes an existing organization from Agendor. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Agendor by ID. |
| [List Organizations](actions/list-organizations.md) | GET | Finds organizations in Agendor by search filters. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Agendor. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Agendor. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from Agendor. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Agendor by ID. |
| [List People](actions/list-people.md) | GET | Finds people in Agendor by search filters. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Agendor. |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal For Organization](actions/create-deal-for-organization.md) | POST | Creates a new deal for an organization in Agendor. |
| [Create Deal For Person](actions/create-deal-for-person.md) | POST | Creates a new deal for a person in Agendor. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Agendor. |

