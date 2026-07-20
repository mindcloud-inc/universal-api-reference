# Hunter: Native API Reference

A consolidated summary of Hunter's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://hunter.io/api-documentation/v2
- **API base URL:** `https://api.hunter.io/v2`

## Authentication

### API Key

Connect with a Hunter API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://hunter.io/api-documentation/v2#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Sequence Recipient](actions/add-sequence-recipient.md) | `POST /campaigns/:campaignId/recipients` | [docs](https://hunter.io/api-documentation/v2#create-recipient) |
| [Cancel Scheduled Sequence Emails](actions/cancel-scheduled-sequence-emails.md) | `DELETE /campaigns/:campaignId/recipients` | [docs](https://hunter.io/api-documentation/v2#cancel-scheduled-emails) |
| [Count Domain Emails](actions/count-domain-emails.md) | `GET /email-count` | [docs](https://hunter.io/api-documentation/v2#email-count) |
| [Create Custom Attribute](actions/create-custom-attribute.md) | `POST /leads_custom_attributes` | [docs](https://hunter.io/api-documentation/v2#create-custom-attribute) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://hunter.io/api-documentation/v2#create-lead) |
| [Create Leads List](actions/create-leads-list.md) | `POST /leads_lists` | [docs](https://hunter.io/api-documentation/v2#create-leads-list) |
| [Delete Custom Attribute](actions/delete-custom-attribute.md) | `DELETE /leads_custom_attributes/:customAttributeId` | [docs](https://hunter.io/api-documentation/v2#custom-attributes) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /leads/:leadId` | [docs](https://hunter.io/api-documentation/v2#delete-lead) |
| [Delete Leads List](actions/delete-leads-list.md) | `DELETE /leads_lists/:leadsListId` | [docs](https://hunter.io/api-documentation/v2#delete-leads-list) |
| [Discover Companies](actions/discover-companies.md) | `POST /discover` | [docs](https://hunter.io/api-documentation/v2#discover) |
| [Enrich Company](actions/enrich-company.md) | `GET /companies/find` | [docs](https://hunter.io/api-documentation/v2#company-enrichment) |
| [Enrich Person](actions/enrich-person.md) | `GET /people/find` | [docs](https://hunter.io/api-documentation/v2#email-enrichment) |
| [Find Email](actions/find-email.md) | `GET /email-finder` | [docs](https://hunter.io/api-documentation/v2#email-finder) |
| [Get Account Information](actions/get-account-information.md) | `GET /account` | [docs](https://hunter.io/api-documentation/v2#account) |
| [Get Combined Enrichment](actions/get-combined-enrichment.md) | `GET /combined/find` | [docs](https://hunter.io/api-documentation/v2#combined-enrichment) |
| [Get Custom Attribute](actions/get-custom-attribute.md) | `GET /leads_custom_attributes/:customAttributeId` | [docs](https://hunter.io/api-documentation/v2#get-custom-attribute) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:leadId` | [docs](https://hunter.io/api-documentation/v2#get-lead) |
| [Get Leads List](actions/get-leads-list.md) | `GET /leads_lists/:leadsListId` | [docs](https://hunter.io/api-documentation/v2#get-leads-list) |
| [List Custom Attributes](actions/list-custom-attributes.md) | `GET /leads_custom_attributes` | [docs](https://hunter.io/api-documentation/v2#list-custom-attributes) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://hunter.io/api-documentation/v2#list-leads) |
| [List Leads Lists](actions/list-leads-lists.md) | `GET /leads_lists` | [docs](https://hunter.io/api-documentation/v2#list-leads-lists) |
| [List Sequence Recipients](actions/list-sequence-recipients.md) | `GET /campaigns/:campaignId/recipients` | [docs](https://hunter.io/api-documentation/v2#list-recipients) |
| [List Sequences](actions/list-sequences.md) | `GET /campaigns` | [docs](https://hunter.io/api-documentation/v2#list-campaigns) |
| [Search Domain Emails](actions/search-domain-emails.md) | `GET /domain-search` | [docs](https://hunter.io/api-documentation/v2#domain-search) |
| [Start Sequence](actions/start-sequence.md) | `POST /campaigns/:campaignId/start` | [docs](https://hunter.io/api-documentation/v2#start-campaign) |
| [Update Custom Attribute](actions/update-custom-attribute.md) | `PUT /leads_custom_attributes/:customAttributeId` | [docs](https://hunter.io/api-documentation/v2#update-custom-attribute) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/:leadId` | [docs](https://hunter.io/api-documentation/v2#update-lead) |
| [Update Leads List](actions/update-leads-list.md) | `PUT /leads_lists/:leadsListId` | [docs](https://hunter.io/api-documentation/v2#update-leads-list) |
| [Upsert Lead](actions/upsert-lead.md) | `PUT /leads` | [docs](https://hunter.io/api-documentation/v2#upsert-lead) |
| [Verify Email](actions/verify-email.md) | `GET /email-verifier` | [docs](https://hunter.io/api-documentation/v2#email-verifier) |
