# <img src="https://images.mindcloud.co/apps/icons/salesmate_1773694413157.png" alt="Salesmate logo" width="28" height="28"> Salesmate: Universal API

Manage contacts, companies, deals, activities, and notes in Salesmate

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesmate/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.salesmate.io
- **Vendor API docs:** https://apidocs.salesmate.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Active Users](actions/get-active-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-active-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Add Activity](actions/add-activity.md) | POST |  |
| [Delete Activity](actions/delete-activity.md) | DELETE |  |
| [Get Activity](actions/get-activity.md) | GET |  |
| [Search Activities](actions/search-activities.md) | GET |  |
| [Update Activity](actions/update-activity.md) | PUT |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Add Company](actions/add-company.md) | POST |  |
| [Delete Company](actions/delete-company.md) | DELETE |  |
| [Get Company](actions/get-company.md) | GET |  |
| [Search Companies](actions/search-companies.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Search Contacts](actions/search-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Add Deal](actions/add-deal.md) | POST |  |
| [Delete Deal](actions/delete-deal.md) | DELETE |  |
| [Get Deal](actions/get-deal.md) | GET |  |
| [Search Deals](actions/search-deals.md) | GET |  |
| [Update Deal](actions/update-deal.md) | PUT |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Add Company Note](actions/add-company-note.md) | POST |  |
| [Add Contact Note](actions/add-contact-note.md) | POST |  |
| [Add Deal Note](actions/add-deal-note.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Users](actions/get-active-users.md) | GET |  |

