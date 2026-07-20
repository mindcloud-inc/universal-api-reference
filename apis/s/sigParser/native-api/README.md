# SigParser: Native API Reference

A consolidated summary of SigParser's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://ipaas.sigparser.com/
- **OpenAPI specification:** https://ipaas.sigparser.com/swagger/v1/swagger.json
- **API base URL:** `https://ipaas.sigparser.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://ipaas.sigparser.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `take` in the query string to set the page size (default 100; accepted range 25–250). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /api/Webhooks` | [docs](https://ipaas.sigparser.com/v1#post-api-webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/Webhooks` | [docs](https://ipaas.sigparser.com/v1#delete-api-webhooks) |
| [Get Company By Domain](actions/get-company-by-domain.md) | `GET /api/Companies` | [docs](https://ipaas.sigparser.com/v1#get-api-companies) |
| [Get Contact By Email](actions/get-contact-by-email.md) | `POST /api/Contacts/List` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts-list) |
| [Get Contact-to-Company Interaction Graph](actions/get-contact-to-company-interaction-graph.md) | `POST /api/Contacts/CompaniesGraph` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts-companiesgraph) |
| [Get Contact-to-Contact Interaction Graph](actions/get-contact-to-contact-interaction-graph.md) | `POST /api/Contacts/ContactsGraph` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts-contactsgraph) |
| [Get Current User](actions/get-current-user.md) | `GET /api/User/Me` | [docs](https://ipaas.sigparser.com/) |
| [Get Email By Message ID](actions/get-email-by-message-id.md) | `GET /api/Emails/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-emails-distinct) |
| [Get Meeting By ICalUID](actions/get-meeting-by-i-cal-uid.md) | `GET /api/Meetings/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-meetings-distinct) |
| [Get Webhook By ID](actions/get-webhook-by-id.md) | `GET /api/Webhooks` | [docs](https://ipaas.sigparser.com/v1#get-api-webhooks) |
| [List Companies](actions/list-companies.md) | `GET /api/Companies` | [docs](https://ipaas.sigparser.com/v1#get-api-companies) |
| [List Contacts](actions/list-contacts.md) | `POST /api/Contacts/List` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts-list) |
| [List Contacts By Company Domain](actions/list-contacts-by-company-domain.md) | `POST /api/Contacts/List` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts-list) |
| [List Contacts With Relationship Metrics](actions/list-contacts-with-relationship-metrics.md) | `POST /api/Contacts/List` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts-list) |
| [List Distinct Emails](actions/list-distinct-emails.md) | `GET /api/Emails/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-emails-distinct) |
| [List Distinct Meetings](actions/list-distinct-meetings.md) | `GET /api/Meetings/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-meetings-distinct) |
| [List Emails By Contact](actions/list-emails-by-contact.md) | `GET /api/Emails/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-emails-distinct) |
| [List Meetings By Attendee Email](actions/list-meetings-by-attendee-email.md) | `GET /api/Meetings/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-meetings-distinct) |
| [List Newly Ingested Emails](actions/list-newly-ingested-emails.md) | `GET /api/Emails/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-emails-distinct) |
| [List Updated Companies](actions/list-updated-companies.md) | `GET /api/Companies` | [docs](https://ipaas.sigparser.com/v1#get-api-companies) |
| [List Updated Contacts](actions/list-updated-contacts.md) | `POST /api/Contacts/List` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts-list) |
| [List Updated Meetings](actions/list-updated-meetings.md) | `GET /api/Meetings/Distinct` | [docs](https://ipaas.sigparser.com/v1#get-api-meetings-distinct) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/Webhooks/List` | [docs](https://ipaas.sigparser.com/v1#get-api-webhooks-list) |
| [Parse Signature From JSON](actions/parse-signature-from-json.md) | `POST /api/Parse/Email/Contact/JSON` | [docs](https://ipaas.sigparser.com/v1#post-api-parse-email-contact-json) |
| [Parse Signature From MIME/EML](actions/parse-signature-from-mime-eml.md) | `POST /api/Parse/Email/Contact/MIME` | [docs](https://ipaas.sigparser.com/v1#post-api-parse-email-contact-mime) |
| [Parse Signature From MSG](actions/parse-signature-from-msg.md) | `POST /api/Parse/Email/Contact/MSG` | [docs](https://ipaas.sigparser.com/v1#post-api-parse-email-contact-msg) |
| [Revoke Current API Key](actions/revoke-current-api-key.md) | `DELETE /api/User/Invalidate` | [docs](https://ipaas.sigparser.com/v1#delete-api-user-invalidate) |
| [Split Email From MIME/EML](actions/split-email-from-mime-eml.md) | `POST /api/Parse/Email/Message/MIME` | [docs](https://ipaas.sigparser.com/v1#post-api-parse-email-message-mime) |
| [Split Email From MSG](actions/split-email-from-msg.md) | `POST /api/Parse/Email/Message/MSG` | [docs](https://ipaas.sigparser.com/v1#post-api-parse-email-message-msg) |
| [Upsert Contact](actions/upsert-contact.md) | `POST /api/Contacts` | [docs](https://ipaas.sigparser.com/v1#post-api-contacts) |
