# GetSales.io: Native API Reference

A consolidated summary of GetSales.io's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.getsales.io/
- **OpenAPI specification:** https://api.getsales.io/_spec/api/openapi.json?download=
- **API base URL:** `https://amazing.getsales.io`

## Authentication

### API Key

Authenticate GetSales.io API requests with an API key sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.getsales.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order_field` in the query string. Set the direction separately with `order_type`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To Automation](actions/add-contact-to-automation.md) | `POST /flows/api/flows/{flowUuid}/leads/{leadUuid}` | [docs](https://api.getsales.io/api/openapi/automations/addleadtoflow.md) |
| [Add New Contact To Automation](actions/add-new-contact-to-automation.md) | `POST /flows/api/flows/{flowUuid}/add-new-lead` | [docs](https://api.getsales.io/api/openapi/automations/addnewleadtoflow.md) |
| [Cancel Contact From All Automations](actions/cancel-contact-from-all-automations.md) | `PUT /flows/api/flows/leads/{leadUuid}/cancel-all` | [docs](https://api.getsales.io/api/openapi/automations/cancelleadfromallflows.md) |
| [Cancel Contact From Automations](actions/cancel-contact-from-automations.md) | `PUT /flows/api/flows/leads/{leadUuid}/cancel` | [docs](https://api.getsales.io/api/openapi/automations/cancelleadfromflows.md) |
| [Connect Sender Profile With GoLogin](actions/connect-sender-profile-with-go-login.md) | `POST /flows/client-api/sender-profiles/connect-external` | [docs](https://api.getsales.io/api/openapi/sender-profiles/connectsenderprofile.md) |
| [Create Contacts](actions/create-contacts.md) | `POST /leads/api/leads` | [docs](https://api.getsales.io/) |
| [Create List](actions/create-list.md) | `POST /leads/api/lists` | [docs](https://api.getsales.io/api/openapi/lists/createlist.md) |
| [Create Sender Profile](actions/create-sender-profile.md) | `POST /flows/api/sender-profiles` | [docs](https://api.getsales.io/api/openapi/sender-profiles/createsenderprofile.md) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /leads/api/leads/{uuid}` | [docs](https://api.getsales.io/api/openapi/contacts/deletelead.md) |
| [Find Contact](actions/find-contact.md) | `POST /leads/api/leads/lookup-one` | [docs](https://api.getsales.io/api/openapi/contacts/findonecontact.md) |
| [Get Contact](actions/get-contact.md) | `GET /leads/api/leads/{uuid}` | [docs](https://api.getsales.io/api/openapi/contacts/getlead.md) |
| [Get List](actions/get-list.md) | `GET /leads/api/lists/{uuid}` | [docs](https://api.getsales.io/api/openapi/lists/getlist.md) |
| [Get Sender Profile](actions/get-sender-profile.md) | `GET /flows/api/sender-profiles/{senderProfileUuid}` | [docs](https://api.getsales.io/api/openapi/sender-profiles/getsenderprofile.md) |
| [List Automations](actions/list-automations.md) | `GET /flows/api/flows` | [docs](https://api.getsales.io/api/openapi/automations/listflows.md) |
| [List Emails](actions/list-emails.md) | `GET /emails/api/emails` | [docs](https://api.getsales.io/api/openapi/unibox/listemails.md) |
| [List LinkedIn Messages](actions/list-linked-in-messages.md) | `GET /flows/api/linkedin-messages` | [docs](https://api.getsales.io/api/openapi/unibox/listlinkedinmessages.md) |
| [List Lists](actions/list-lists.md) | `GET /leads/api/lists` | [docs](https://api.getsales.io/api/openapi/lists/listlists.md) |
| [List Sender Profiles](actions/list-sender-profiles.md) | `GET /flows/api/sender-profiles` | [docs](https://api.getsales.io/api/openapi/sender-profiles/listsenderprofiles.md) |
| [List Contacts](actions/search-contacts.md) | `POST /leads/api/leads/search` | [docs](https://api.getsales.io/api/openapi/contacts/searchcontacts.md) |
| [Send Email](actions/send-email.md) | `POST /emails/api/emails/send-email` | [docs](https://api.getsales.io/api/openapi/unibox/sendemail.md) |
| [Send LinkedIn Message](actions/send-linked-in-message.md) | `POST /flows/api/linkedin-messages` | [docs](https://api.getsales.io/api/openapi/unibox/sendlinkedinmessage.md) |
| [Start Automation](actions/start-automation.md) | `PUT /flows/api/flows/{flowUuid}/start` | [docs](https://api.getsales.io/api/openapi/automations/startflow.md) |
| [Stop Automation](actions/stop-automation.md) | `PUT /flows/api/flows/{flowUuid}/stop` | [docs](https://api.getsales.io/api/openapi/automations/stopflow.md) |
| [Update Contact](actions/update-contact.md) | `PUT /leads/api/leads/{uuid}` | [docs](https://api.getsales.io/api/openapi/contacts/updatelead.md) |
| [Create Or Update Contact](actions/upsert-contact.md) | `POST /leads/api/leads/upsert` | [docs](https://api.getsales.io/api/openapi/contacts/upsertcontact.md) |
