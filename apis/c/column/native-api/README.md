# Column: Native API Reference

A consolidated summary of Column's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://column.com/docs/api/
- **API base URL:** `https://api.column.com`

## Authentication

### Basic auth

Authenticate Column requests with basic auth.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://column.com/docs/workingwithapi)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `institutions`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `starting_after` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel ACH Transfer](actions/cancel-ach-transfer.md) | `POST /transfers/ach/:ach_transfer_id/cancel` | [docs](https://column.com/docs/api/#ach-transfer/cancel) |
| [Cancel Book Transfer](actions/cancel-book-transfer.md) | `POST /transfers/book/:book_transfer_id/cancel` | [docs](https://column.com/docs/api/#book-transfer/cancel) |
| [Create Account Number](actions/create-account-number.md) | `POST /bank-accounts/:bank_account_id/account-numbers` | [docs](https://column.com/docs/api/#account-number/create) |
| [Create ACH Transfer](actions/create-ach-transfer.md) | `POST /transfers/ach` | [docs](https://column.com/docs/api/#ach-transfer/create) |
| [Create Bank Account](actions/create-bank-account.md) | `POST /bank-accounts` | [docs](https://column.com/docs/api/#bank-account/create) |
| [Create Book Transfer](actions/create-book-transfer.md) | `POST /transfers/book` | [docs](https://column.com/docs/api/#book-transfer/create) |
| [Create Business Entity](actions/create-business-entity.md) | `POST /entities/business` | [docs](https://column.com/docs/api/#entity/create-business) |
| [Create Counterparty](actions/create-counterparty.md) | `POST /counterparties` | [docs](https://column.com/docs/api/#counterparty/create) |
| [Create Evidence With File Upload](actions/create-evidence-with-file-upload.md) | `POST /entities/:entity_id/evidence` | [docs](https://column.com/docs/api/#entity/create-evidence-with-upload) |
| [Create Person Entity](actions/create-person-entity.md) | `POST /entities/person` | [docs](https://column.com/docs/api/#entity/create-person) |
| [Create Wire Transfer](actions/create-wire-transfer.md) | `POST /transfers/wire` | [docs](https://column.com/docs/api/#wire-transfer/create) |
| [Get ACH Transfer](actions/get-ach-transfer.md) | `GET /transfers/ach/:ach_transfer_id` | [docs](https://column.com/docs/api/#ach-transfer/get) |
| [Get Additional Requirements](actions/get-additional-requirements.md) | `GET /entities/:entity_id/additional-requirements` | [docs](https://column.com/docs/api/#entity/get-additional-requirements) |
| [Get Bank Account](actions/get-bank-account.md) | `GET /bank-accounts/:bank_account_id` | [docs](https://column.com/docs/api/#bank-account/get-id) |
| [Get Book Transfer](actions/get-book-transfer.md) | `GET /transfers/book/:book_transfer_id` | [docs](https://column.com/docs/api/#book-transfer/get) |
| [Get Counterparty](actions/get-counterparty.md) | `GET /counterparties/:counterparty_id` | [docs](https://column.com/docs/api/#counterparty/get-id) |
| [Get Document](actions/get-document.md) | `GET /documents/:document_id` | [docs](https://column.com/docs/api/#documents/get) |
| [Get Entity](actions/get-entity.md) | `GET /entities/:entity_id` | [docs](https://column.com/docs/api/#entity/get-id) |
| [Get Entity Compliance](actions/get-entity-compliance.md) | `GET /entities/:entity_id/compliance` | [docs](https://column.com/docs/api/#entity/get-entity-compliance) |
| [Get Financial Institution](actions/get-financial-institution.md) | `GET /institutions/:routing_number` | [docs](https://column.com/docs/api/#counterparty/get-institution) |
| [Get Wire Transfer](actions/get-wire-transfer.md) | `GET /transfers/wire/:wire_transfer_id` | [docs](https://column.com/docs/api/#wire-transfer/get) |
| [Link Associated Person](actions/link-associated-person.md) | `POST /entities/:entity_id/associated-persons` | [docs](https://column.com/docs/api/#entity/link-associated-person) |
| [List Account Numbers](actions/list-account-numbers.md) | `GET /bank-accounts/:bank_account_id/account-numbers` | [docs](https://column.com/docs/api/#account-number/list-all) |
| [List ACH Transfers](actions/list-ach-transfers.md) | `GET /transfers/ach` | [docs](https://column.com/docs/api/#ach-transfer/list-all) |
| [List All Transfers](actions/list-all-transfers.md) | `GET /transfers` | [docs](https://column.com/docs/api/#transfer/list-all) |
| [List Associated Persons](actions/list-associated-persons.md) | `GET /entities/:entity_id/associated-persons` | [docs](https://column.com/docs/api/#entity/get-associated-persons) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /bank-accounts` | [docs](https://column.com/docs/api/#bank-account/list-all) |
| [List Book Transfers](actions/list-book-transfers.md) | `GET /transfers/book` | [docs](https://column.com/docs/api/#book-transfer/list-all) |
| [List Counterparties](actions/list-counterparties.md) | `GET /counterparties` | [docs](https://column.com/docs/api/#counterparty/list-all) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://column.com/docs/api/#documents/list-all) |
| [List Entities](actions/list-entities.md) | `GET /entities` | [docs](https://column.com/docs/api/#entity/list-all) |
| [List Entity Evidence](actions/list-entity-evidence.md) | `GET /entities/:entity_id/evidence` | [docs](https://column.com/docs/api/#entity/get-entity-evidence) |
| [List Financial Institutions](actions/list-financial-institutions.md) | `GET /institutions` | [docs](https://column.com/docs/api/) |
| [List Wire Transfers](actions/list-wire-transfers.md) | `GET /transfers/wire` | [docs](https://column.com/docs/api/#wire-transfer/list-all) |
| [Reverse ACH Transfer](actions/reverse-ach-transfer.md) | `POST /transfers/ach/:ach_transfer_id/reverse` | [docs](https://column.com/docs/api/#ach-transfer/reverse) |
| [Submit Additional Requirements](actions/submit-additional-requirements.md) | `POST /entities/:entity_id/additional-requirements` | [docs](https://column.com/docs/api/#entity/submit-additional-requirements) |
| [Update Bank Account](actions/update-bank-account.md) | `PATCH /bank-accounts/:bank_account_id` | [docs](https://column.com/docs/api/#bank-account/update) |
| [Update Business Entity](actions/update-business-entity.md) | `PATCH /entities/business/:entity_id` | [docs](https://column.com/docs/api/#entity/update-business) |
| [Update Person Entity](actions/update-person-entity.md) | `PATCH /entities/person/:entity_id` | [docs](https://column.com/docs/api/#entity/update-person) |
| [Upload Document](actions/upload-document.md) | `POST /documents` | [docs](https://column.com/docs/api/#documents/upload) |
