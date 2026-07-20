# DialMyCalls: Native API Reference

A consolidated summary of DialMyCalls's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://www.dialmycalls.com/api-documentation
- **API base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`

## Authentication

### API Key

Connect DialMyCalls with your API key.

### Credentials

- **API Key:** `apiKey` · required · Your DialMyCalls API key from Integrations > API Info.

[Official authentication documentation](https://www.dialmycalls.com/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string to choose the result range; numbering starts at 0.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Caller ID](actions/add-caller-id.md) | `POST /callerid` | [docs](https://www.dialmycalls.com/api-documentation#callerid-add) |
| [Add Contact](actions/add-contact.md) | `POST /contact` | [docs](https://www.dialmycalls.com/api-documentation#contact-add) |
| [Add Group](actions/add-group.md) | `POST /group` | [docs](https://www.dialmycalls.com/api-documentation#group-add) |
| [Cancel Call](actions/cancel-call.md) | `DELETE /service/call/:CallId` | [docs](https://www.dialmycalls.com/api-documentation#call-cancel) |
| [Cancel Text](actions/cancel-text.md) | `DELETE /service/text/:TextId` | [docs](https://www.dialmycalls.com/api-documentation#text-cancel) |
| [Create Call](actions/create-call.md) | `POST /service/call` | [docs](https://www.dialmycalls.com/api-documentation#call-create) |
| [Create Recording (Text-to-Speech)](actions/create-recording-text-to-speech.md) | `POST /recording/tts` | [docs](https://www.dialmycalls.com/api-documentation#recording-create-tts) |
| [Create Text](actions/create-text.md) | `POST /service/text` | [docs](https://www.dialmycalls.com/api-documentation#text-create) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/:ContactId` | [docs](https://www.dialmycalls.com/api-documentation#contact-delete) |
| [Delete Group](actions/delete-group.md) | `DELETE /group/:GroupId` | [docs](https://www.dialmycalls.com/api-documentation#group-delete) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://www.dialmycalls.com/api-documentation#account-get) |
| [Get Call](actions/get-call.md) | `GET /service/call/:CallId` | [docs](https://www.dialmycalls.com/api-documentation#call-get) |
| [Get Caller ID](actions/get-caller-id.md) | `GET /callerid/:CalleridId` | [docs](https://www.dialmycalls.com/api-documentation#callerid-get) |
| [Get Contact](actions/get-contact.md) | `GET /contact/:ContactId` | [docs](https://www.dialmycalls.com/api-documentation#contact-get) |
| [Get Group](actions/get-group.md) | `GET /group/:GroupId` | [docs](https://www.dialmycalls.com/api-documentation#group-get) |
| [Get Recording](actions/get-recording.md) | `GET /recording/:RecordingId` | [docs](https://www.dialmycalls.com/api-documentation#recording-get) |
| [Get Text](actions/get-text.md) | `GET /service/text/:TextId` | [docs](https://www.dialmycalls.com/api-documentation#text-get) |
| [List Caller IDs](actions/list-caller-ids.md) | `GET /callerids` | [docs](https://www.dialmycalls.com/api-documentation#callerids-get) |
| [List Calls](actions/list-calls.md) | `GET /service/calls` | [docs](https://www.dialmycalls.com/api-documentation#calls-get) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.dialmycalls.com/api-documentation#contacts-get) |
| [List Contacts in Group](actions/list-contacts-in-group.md) | `GET /contacts/:GroupId` | [docs](https://www.dialmycalls.com/api-documentation#contacts-get-group) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://www.dialmycalls.com/api-documentation#groups-get) |
| [List Keywords](actions/list-keywords.md) | `GET /keywords` | [docs](https://www.dialmycalls.com/api-documentation#keywords-get) |
| [List Recordings](actions/list-recordings.md) | `GET /recordings` | [docs](https://www.dialmycalls.com/api-documentation#recordings-get) |
| [List Texts](actions/list-texts.md) | `GET /service/texts` | [docs](https://www.dialmycalls.com/api-documentation#texts-get) |
| [List Vanity Numbers](actions/list-vanity-numbers.md) | `GET /vanitynumbers` | [docs](https://www.dialmycalls.com/api-documentation#vanitynumbers-get) |
| [Update Caller ID](actions/update-caller-id.md) | `PUT /callerid/:CalleridId` | [docs](https://www.dialmycalls.com/api-documentation#callerid-update) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/:ContactId` | [docs](https://www.dialmycalls.com/api-documentation#contact-update) |
| [Update Group](actions/update-group.md) | `PUT /group/:GroupId` | [docs](https://www.dialmycalls.com/api-documentation#group-update) |
