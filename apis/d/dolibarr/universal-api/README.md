# <img src="https://images.mindcloud.co/apps/icons/images-25_1776795002896.png" alt="Dolibarr logo" width="28" height="28"> Dolibarr: Universal API

Dolibarr is an open-source ERP and CRM suite for managing business operations such as users, company setup, agenda events, categories, documents, and other enabled Dolibarr modules through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dolibarr/latest
- **Category:** Commerce / ERP
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dolibarr.org/
- **Vendor API docs:** https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Status](actions/get-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Enabled Modules](actions/list-enabled-modules.md) | GET | Retrieves a list of enabled modules from Dolibarr. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Agenda Event](actions/get-agenda-event.md) | GET | Retrieves an agenda event from Dolibarr. |
| [List Agenda Events](actions/list-agenda-events.md) | GET | Retrieves a list of agenda events from Dolibarr. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Dolibarr. |
| [List Categories](actions/list-categories.md) | GET | Retrieves a list of categories from Dolibarr. |
| [List Object Categories](actions/list-object-categories.md) | GET | Retrieves categories for an object in Dolibarr. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Setup](actions/get-company-setup.md) | GET | Retrieves company properties from Dolibarr. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents for a specific Dolibarr record. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Template](actions/get-email-template.md) | GET | Retrieves an email template from Dolibarr. |
| [Get Email Template By Label](actions/get-email-template-by-label.md) | GET | Retrieves an email template from Dolibarr by label. |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves a list of email templates from Dolibarr. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get User Group](actions/get-user-group.md) | GET | Retrieves a user group from Dolibarr. |
| [List Current User Groups](actions/list-current-user-groups.md) | GET | Retrieves the current user's groups from Dolibarr. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Country](actions/get-country.md) | GET | Retrieves a country from Dolibarr. |
| [Get Country By Code](actions/get-country-by-code.md) | GET | Retrieves a country from Dolibarr by code. |
| [Get Country By ISO](actions/get-country-by-iso.md) | GET | Retrieves a country from Dolibarr by ISO code. |
| [Get State](actions/get-state.md) | GET | Retrieves a state or province from Dolibarr. |
| [List Countries](actions/list-countries.md) | GET | Retrieves a list of countries from Dolibarr. |
| [List States](actions/list-states.md) | GET | Retrieves a list of states from Dolibarr. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Status](actions/get-status.md) | GET | Retrieves status information for the Dolibarr instance. |

### Triggers

| Action | Method | Description |
| --- | --- | --- |
| [List Action Triggers](actions/list-action-triggers.md) | GET | Retrieves a list of action triggers from Dolibarr. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Object Link](actions/get-object-link.md) | GET | Retrieves an object link from Dolibarr. |
| [List Category Objects](actions/list-category-objects.md) | GET | Retrieves objects from a Dolibarr category. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves a list of currencies from Dolibarr. |
| [List Object Links](actions/list-object-links.md) | GET | Retrieves object links from Dolibarr by linked object values. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Info](actions/get-current-user-info.md) | GET | Retrieves the current user's details from Dolibarr. |
| [Get User](actions/get-user.md) | GET | Retrieves a user record from Dolibarr. |
| [Get User By Email](actions/get-user-by-email.md) | GET | Retrieves a user from Dolibarr by email address. |
| [Get User By Login](actions/get-user-by-login.md) | GET | Retrieves a user from Dolibarr by login. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Dolibarr. |

