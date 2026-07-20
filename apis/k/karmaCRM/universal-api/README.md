# <img src="https://images.mindcloud.co/apps/icons/karma-crm_1774544249656.png" alt="Karma CRM logo" width="28" height="28"> Karma CRM: Universal API

Manage customers, tasks, and sales workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/karmaCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.karmacrm.com/
- **Vendor API docs:** https://docs.karmacrm.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Social Account Types](actions/list-social-account-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-social-account-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in Karma CRM. |
| [Delete Activity](actions/delete-activity.md) | DELETE | Deletes an existing activity from Karma CRM. |
| [Get Activity](actions/get-activity.md) | GET | Retrieves a specific activity from Karma CRM. |
| [List Activities](actions/list-activities.md) | GET | Retrieves a list of activities from Karma CRM. |
| [List Related Activities](actions/list-related-activities.md) | GET | Retrieves activities related to a contact in Karma CRM. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in Karma CRM. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment](actions/create-attachment.md) | POST | Creates an attachment in Karma CRM. |

### Authorization

| Action | Method | Description |
| --- | --- | --- |
| [List Authorizations](actions/list-authorizations.md) | GET | Retrieves integration authorizations from Karma CRM. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a new calendar in Karma CRM. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves a list of calendars from Karma CRM. |
| [Update Calendar](actions/update-calendar.md) | PUT | Updates an existing calendar in Karma CRM. |

### Campaign Entry

| Action | Method | Description |
| --- | --- | --- |
| [Apply Campaign](actions/apply-campaign.md) | POST | Applies a campaign to a record in Karma CRM. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Karma CRM. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Karma CRM. |
| [Get Company](actions/get-company.md) | GET | Retrieves a specific company from Karma CRM. |
| [List Companies](actions/list-companies.md) | GET | Retrieves a list of companies from Karma CRM. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Karma CRM. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Karma CRM. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Karma CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a specific contact from Karma CRM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Karma CRM. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Karma CRM. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Karma CRM. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Karma CRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a specific deal from Karma CRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves a list of deals from Karma CRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Karma CRM. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Delete Email Draft](actions/delete-email-draft.md) | DELETE | Deletes an email draft from Karma CRM. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Notes](actions/list-notes.md) | GET | Retrieves note histories from Karma CRM. |

### Social Account Type

| Action | Method | Description |
| --- | --- | --- |
| [List Social Account Types](actions/list-social-account-types.md) | GET | Retrieves social account types from Karma CRM. |

