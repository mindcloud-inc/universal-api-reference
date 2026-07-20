# Karma CRM: Native API Reference

A consolidated summary of Karma CRM's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.karmacrm.com/
- **API base URL:** `https://app.karmacrm.com`

## Authentication

### API Token

Use the karmaCRM api_token returned by the sign-in endpoint.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.karmacrm.com/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Campaign](actions/apply-campaign.md) | `POST /api/v3/campaign_entries/apply` | [docs](https://docs.karmacrm.com/#apply-campaign-create-a-campaign-entries) |
| [Create Activity](actions/create-activity.md) | `POST /api/v3/activities.json` | [docs](https://docs.karmacrm.com/#create-an-activity) |
| [Create Attachment](actions/create-attachment.md) | `POST /api/v2/attachments` | [docs](https://docs.karmacrm.com/#create-an-attachment) |
| [Create Calendar](actions/create-calendar.md) | `POST /api/v3/calendars.json` | [docs](https://docs.karmacrm.com/#create-a-calendar) |
| [Create Company](actions/create-company.md) | `POST /api/v3/companies.json` | [docs](https://docs.karmacrm.com/#create-a-company) |
| [Create Contact](actions/create-contact.md) | `POST /api/v3/contacts.json` | [docs](https://docs.karmacrm.com/#create-a-contact) |
| [Create Deal](actions/create-deal.md) | `POST /api/v3/deals.json` | [docs](https://docs.karmacrm.com/#create-a-deal) |
| [Delete Activity](actions/delete-activity.md) | `DELETE /api/v3/activities/:id.json` | [docs](https://docs.karmacrm.com/#delete-a-activity) |
| [Delete Company](actions/delete-company.md) | `DELETE /api/v2/companies/:id.json` | [docs](https://docs.karmacrm.com/#delete-a-company) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/v3/contacts/:id.json` | [docs](https://docs.karmacrm.com/#delete-a-contact) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /api/v2/deals/:id.json` | [docs](https://docs.karmacrm.com/#delete-a-deal) |
| [Delete Email Draft](actions/delete-email-draft.md) | `DELETE /api/v3/mailman_nylas/outgoing/messages/:id.json` | [docs](https://docs.karmacrm.com/#delete-an-email-draft) |
| [Get Activity](actions/get-activity.md) | `GET /api/v3/activities/:id.json` | [docs](https://docs.karmacrm.com/#get-a-specific-activity) |
| [Get Company](actions/get-company.md) | `GET /api/v3/companies/:id.json` | [docs](https://docs.karmacrm.com/#get-a-specific-company) |
| [Get Contact](actions/get-contact.md) | `GET /api/v3/contacts/:id.json` | [docs](https://docs.karmacrm.com/#get-a-specific-contact) |
| [Get Deal](actions/get-deal.md) | `GET /api/v3/deals/:id.json` | [docs](https://docs.karmacrm.com/#get-a-specific-deal) |
| [List Activities](actions/list-activities.md) | `GET /api/v3/activities.json` | [docs](https://docs.karmacrm.com/#get-all-activities) |
| [List Authorizations](actions/list-authorizations.md) | `GET /api/v2/settings/integrations.json` | [docs](https://docs.karmacrm.com/#get-all-authorizations) |
| [List Calendars](actions/list-calendars.md) | `GET /api/v3/calendars.json` | [docs](https://docs.karmacrm.com/#get-all-calendars) |
| [List Companies](actions/list-companies.md) | `GET /api/v3/companies.json` | [docs](https://docs.karmacrm.com/#get-all-companies) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v3/contacts.json` | [docs](https://docs.karmacrm.com/#get-all-contacts) |
| [List Deals](actions/list-deals.md) | `GET /api/v3/deals.json` | [docs](https://docs.karmacrm.com/#get-all-deals) |
| [List Notes](actions/list-notes.md) | `GET /api/v2/histories.json` | [docs](https://docs.karmacrm.com/#get-all-notes-histories) |
| [List Related Activities](actions/list-related-activities.md) | `GET /api/v3/activities/related.json` | [docs](https://docs.karmacrm.com/#get-related-activities-for-a-contact) |
| [List Social Account Types](actions/list-social-account-types.md) | `GET /api/v2/settings/social_account_types.json` | [docs](https://docs.karmacrm.com/#get-all-social-account-types) |
| [Update Activity](actions/update-activity.md) | `PUT /api/v3/activities/:id.json` | [docs](https://docs.karmacrm.com/#update-an-activity) |
| [Update Calendar](actions/update-calendar.md) | `PUT /api/v3/calendars/:id.json` | [docs](https://docs.karmacrm.com/#update-a-calendar) |
| [Update Company](actions/update-company.md) | `PUT /api/v3/companies/:id.json` | [docs](https://docs.karmacrm.com/#update-a-company) |
| [Update Contact](actions/update-contact.md) | `PUT /api/v3/contacts/:id.json` | [docs](https://docs.karmacrm.com/#update-a-contact) |
| [Update Deal](actions/update-deal.md) | `PUT /api/v3/deals/:id.json` | [docs](https://docs.karmacrm.com/#update-a-deal) |
