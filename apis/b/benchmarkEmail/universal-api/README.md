# <img src="https://images.mindcloud.co/apps/icons/benchmark-email_1773858633704.png" alt="Benchmark Email logo" width="28" height="28"> Benchmark Email: Universal API

Create campaigns, manage contacts, and track email performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/benchmarkEmail/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.benchmarkemail.com
- **Vendor API docs:** https://developer.benchmarkemail.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile Details](actions/get-profile-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/get-profile-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation](actions/get-automation.md) | GET | Retrieves an automation from Benchmark Email. |
| [Get Automation Report](actions/get-automation-report.md) | GET | Retrieves an automation report from Benchmark Email. |
| [List Automations](actions/list-automations.md) | GET | Retrieves a list of automations from Benchmark Email. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Details](actions/get-client-details.md) | GET | Retrieves client details from Benchmark Email. |
| [Get Plan](actions/get-plan.md) | GET | Retrieves plan details from Benchmark Email. |
| [Get Profile Details](actions/get-profile-details.md) | GET | Retrieves client profile details from Benchmark Email. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in a Benchmark Email contact list. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from a Benchmark Email contact list. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Benchmark Email contact list. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Benchmark Email by search criteria. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in a Benchmark Email contact list. |

### Contactlist

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a contact list in Benchmark Email. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from Benchmark Email. |
| [List Contact Lists](actions/list-contact-lists.md) | GET |  |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in Benchmark Email. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-email.md) | POST | Creates an email in Benchmark Email. |
| [Get Email](actions/get-email.md) | GET | Retrieves an email from Benchmark Email. |
| [Get Email Preview](actions/get-email-preview.md) | GET | Retrieves an email preview from Benchmark Email. |
| [List Email Reports](actions/list-email-reports.md) | GET | Retrieves a list of email reports from Benchmark Email. |
| [Schedule Email](actions/schedule-email.md) | PUT | Schedules an email in Benchmark Email. |
| [Update Email](actions/update-email.md) | PUT | Updates an existing email in Benchmark Email. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Segment](actions/create-contact-segment.md) | POST | Creates a contact segment in Benchmark Email. |
| [Get Contact Segment](actions/get-contact-segment.md) | GET | Retrieves a contact segment from Benchmark Email. |
| [List Contact Segments](actions/list-contact-segments.md) | GET | Retrieves contact segments from Benchmark Email. |

