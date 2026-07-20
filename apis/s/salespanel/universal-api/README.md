# <img src="https://images.mindcloud.co/apps/icons/salespanel_1774900242261.png" alt="Salespanel logo" width="28" height="28"> Salespanel: Universal API

Track leads, visitors, companies, and activities in Salespanel

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salespanel/latest
- **Category:** Marketing
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salespanel.io/
- **Vendor API docs:** https://salespanel.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Activities](actions/list-contact-activities.md) | GET | Retrieves activities for a contact in Salespanel by ID or email. |
| [Log Custom Activity](actions/log-custom-activity.md) | POST | Creates a custom activity in Salespanel for a visitor. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Visiting Companies](actions/list-visiting-companies.md) | GET | Retrieves visiting companies from your Salespanel account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Identify Contact](actions/identify-contact.md) | PUT | Identifies a contact in Salespanel by associating an email. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Salespanel account. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from your Salespanel account. |
| [Set Visitor Attributes](actions/set-visitor-attributes.md) | PUT | Updates custom visitor attributes in Salespanel. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from your Salespanel account. |

