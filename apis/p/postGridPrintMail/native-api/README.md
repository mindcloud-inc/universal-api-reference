# PostGrid Print & Mail: Native API Reference

A consolidated summary of PostGrid Print & Mail's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.postgrid.com
- **API base URL:** `https://api.postgrid.com/print-mail/v1`

## Authentication

### API Key

Authenticate PostGrid Print & Mail with your PostGrid API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://postgrid.readme.io/docs/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `skip` in the query string as the record offset.

## Retry behavior

Retry responses with status codes `429,503`. Wait 30000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Cheque](actions/cancel-cheque.md) | `DELETE /cheques/{{id}}` | [docs](https://postgrid.readme.io/reference/cheques_delete-1) |
| [Cancel Letter](actions/cancel-letter.md) | `DELETE /letters/{{id}}` | [docs](https://postgrid.readme.io/reference/letters_delete-1) |
| [Cancel Postcard](actions/cancel-postcard.md) | `DELETE /postcards/{{id}}` | [docs](https://postgrid.readme.io/reference/postcards_delete-1) |
| [Create Bank Account](actions/create-bank-account.md) | `POST /bank_accounts` | [docs](https://postgrid.readme.io/reference/bankaccounts_create-1) |
| [Create Cheque](actions/create-cheque.md) | `POST /cheques` | [docs](https://postgrid.readme.io/reference/cheques_create-1) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://postgrid.readme.io/reference/contacts_create-1) |
| [Create Letter](actions/create-letter.md) | `POST /letters` | [docs](https://postgrid.readme.io/reference/letters_create-1) |
| [Create Postcard](actions/create-postcard.md) | `POST /postcards` | [docs](https://postgrid.readme.io/reference/postcards_create-1) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://postgrid.readme.io/reference/templates_create-1) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{{id}}` | [docs](https://postgrid.readme.io/reference/contacts_delete-1) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/{{id}}` | [docs](https://postgrid.readme.io/reference/templates_delete-1) |
| [Get Bank Account](actions/get-bank-account.md) | `GET /bank_accounts/{{id}}` | [docs](https://postgrid.readme.io/reference/bankaccounts_get-1) |
| [Get Cheque](actions/get-cheque.md) | `GET /cheques/{{id}}` | [docs](https://postgrid.readme.io/reference/cheques_get-1) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{{id}}` | [docs](https://postgrid.readme.io/reference/contacts_get-1) |
| [Get Letter](actions/get-letter.md) | `GET /letters/{{id}}` | [docs](https://postgrid.readme.io/reference/letters_get-1) |
| [Get Postcard](actions/get-postcard.md) | `GET /postcards/{{id}}` | [docs](https://postgrid.readme.io/reference/postcards_get-1) |
| [Get Template](actions/get-template.md) | `GET /templates/{{id}}` | [docs](https://postgrid.readme.io/reference/templates_get-1) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /bank_accounts` | [docs](https://postgrid.readme.io/reference/bankaccounts_list-1) |
| [List Cheques](actions/list-cheques.md) | `GET /cheques` | [docs](https://postgrid.readme.io/reference/cheques_list-1) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://postgrid.readme.io/reference/contacts_list-1) |
| [List Letters](actions/list-letters.md) | `GET /letters` | [docs](https://postgrid.readme.io/reference/letters_list-1) |
| [List Postcards](actions/list-postcards.md) | `GET /postcards` | [docs](https://postgrid.readme.io/reference/postcards_list-1) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://postgrid.readme.io/reference/templates_list-1) |
| [Update Template](actions/update-template.md) | `POST /templates/{{id}}` | [docs](https://postgrid.readme.io/reference/templates_update-1) |
