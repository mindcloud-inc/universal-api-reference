# Sage Intacct: Native API Reference

A consolidated summary of Sage Intacct's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://developer.intacct.com/api/
- **API base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`

## Authentication

### Custom

### Credentials

- **Company Id:** `companyId` · required
- **User Id:** `userId` · required
- **User Password:** `userPassword` · required
- **Sender Password:** `senderPassword` · required
- **Sender Id:** `senderId` · required

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

Shared parameters:

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `SenderId` | body | `string` | no |

Responses from this API use XML.

## Pagination

Use `pagesize` in the request body to set the page size (default 100; accepted range 1–1000). Use `offset` in the request body as the record offset.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Budget](actions/create-budget.md) | `POST /` | [docs](https://developer.intacct.com/api/general-ledger/budgets/) |
| [Create File](actions/create-file.md) | `POST` |  |
| [Create Item](actions/create-item.md) | `POST` |  |
| [Create Item New](actions/create-item-2.md) | `POST` |  |
| [Create Bill Item](actions/createbillitem.md) | `POST` |  |
| [Create Journal](actions/createjournal.md) | `POST` | [docs](https://developer.intacct.com/api/accounts-receivable/invoices/#create-invoice-legacy) |
| [Get Custom Object](actions/get-custom-object.md) | `POST` |  |
| [Get Fields for Object](actions/get-fields.md) | `POST` |  |
| [Get Full Item](actions/get-full-item.md) | `POST` |  |
| [Get Full Item By Name](actions/get-full-item-by-name.md) | `POST` |  |
| [List Contacts](actions/list-contacts.md) | `POST /` | [docs](https://developer.intacct.com/api/project-resource-mgmt/projects/#query-and-list-projects) |
| [List Projects](actions/list-projects.md) | `POST /` | [docs](https://developer.intacct.com/api/project-resource-mgmt/projects/#query-and-list-projects) |
| [Read Bank Deposits](actions/new-action1.md) | `POST` |  |
| [Query Object](actions/query-object.md) | `POST /` | [docs](https://developer.intacct.com/web-services/queries/) |
| [Query Object Sum](actions/query-object-sum.md) | `POST` |  |
| [Read By Query](actions/read-by-query.md) | `POST` |  |
| [Update Invoice](actions/update-invoice.md) | `POST` |  |
