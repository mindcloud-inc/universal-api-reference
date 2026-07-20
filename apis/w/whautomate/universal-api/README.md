# <img src="https://images.mindcloud.co/apps/icons/whautomate_1775054468482.png" alt="Whautomate logo" width="28" height="28"> Whautomate: Universal API

Manage contacts, messages, broadcasts, appointments, and WhatsApp automations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whautomate/latest
- **Category:** Support / Contact Center
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whautomate.com
- **Vendor API docs:** https://help.whautomate.com/product-guides/whautomate-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Locations](actions/list-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account information from Whautomate. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in Whautomate. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Whautomate. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Whautomate. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds matching contacts in Whautomate. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Whautomate. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Add Client](actions/add-client.md) | POST | Creates a new client in Whautomate. |
| [Add Tags to Client](actions/add-tags-to-client.md) | PUT | Updates an existing client in Whautomate by adding tags. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Whautomate. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Whautomate. |
| [Remove Tags from Client](actions/remove-tags-from-client.md) | PUT | Updates an existing client in Whautomate by removing tags. |
| [Search Clients](actions/search-clients.md) | GET | Finds matching clients in Whautomate. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Whautomate. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Staff](actions/get-staff.md) | GET | Retrieves a staff member from Whautomate. |
| [List Staffs](actions/list-staffs.md) | GET | Retrieves staff members from Whautomate. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Whautomate. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from Whautomate. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Client Tag](actions/add-client-tag.md) | POST | Creates a new client tag in Whautomate. |
| [Delete Client Tag](actions/delete-client-tag.md) | DELETE | Deletes an existing client tag from Whautomate. |
| [Get Client Tag](actions/get-client-tag.md) | GET | Retrieves a client tag from Whautomate. |
| [List Client Tags](actions/list-client-tags.md) | GET | Retrieves client tags from Whautomate. |

