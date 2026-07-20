# <img src="https://images.mindcloud.co/apps/icons/previsto_1774973389259.png" alt="Previsto logo" width="28" height="28"> Previsto: Universal API

Manage contacts, assignments, service agreements, and account data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/previsto/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://previsto.com
- **Vendor API docs:** https://developer.previsto.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Previsto. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Previsto. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Previsto. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Previsto. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Previsto. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Previsto. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in Previsto. |
| [Retrieve Organization](actions/retrieve-organization.md) | GET | Retrieves an organization from Previsto. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Previsto. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Agreement](actions/create-service-agreement.md) | POST | Creates a new service agreement in Previsto. |
| [Delete Service Agreement](actions/delete-service-agreement.md) | DELETE | Deletes an existing service agreement from Previsto. |
| [Retrieve Service Agreement](actions/retrieve-service-agreement.md) | GET | Retrieves a service agreement from Previsto. |
| [Update Service Agreement](actions/update-service-agreement.md) | PUT | Updates an existing service agreement in Previsto. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Service Agreements](actions/list-service-agreements.md) | GET | Retrieves service agreements from Previsto. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Assignment](actions/create-assignment.md) | POST | Creates a new assignment in Previsto. |
| [Delete Assignment](actions/delete-assignment.md) | DELETE | Deletes an existing assignment from Previsto. |
| [List Assignments](actions/list-assignments.md) | GET | Retrieves assignments from Previsto. |
| [Retrieve Assignment](actions/retrieve-assignment.md) | GET | Retrieves an assignment from Previsto. |
| [Update Assignment](actions/update-assignment.md) | PUT | Updates an existing assignment in Previsto. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current account from Previsto. |

