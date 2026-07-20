# Notifyre SMS: Native API Reference

A consolidated summary of Notifyre SMS's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://docs.notifyre.com/api/introduction
- **API base URL:** `https://api.notifyre.com/20220711`

## Authentication

### API Key

Authenticate with a Notifyre API token using the x-api-token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-token: <apiKey>
```

[Official authentication documentation](https://support.notifyre.com/account-management/how-to-create-an-api-token)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `user-agent` | `20220711` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contacts To Groups](actions/add-contacts-to-groups.md) | `POST /addressbook/groups/contacts` | [docs](https://docs.notifyre.com/api/address-book-contacts-add-to-groups) |
| [Create Contact](actions/create-contact.md) | `POST /addressbook/contacts` | [docs](https://docs.notifyre.com/api/address-book-contact-create) |
| [Create Group](actions/create-group.md) | `POST /addressbook/groups` | [docs](https://docs.notifyre.com/api/address-book-group-create) |
| [Delete Contacts](actions/delete-contacts.md) | `DELETE /addressbook/contacts` | [docs](https://docs.notifyre.com/api/address-book-contacts-delete) |
| [Delete Groups](actions/delete-groups.md) | `DELETE /addressbook/groups` | [docs](https://docs.notifyre.com/api/address-book-group-delete) |
| [Download MMS Reply](actions/download-mms-reply.md) | `GET /mms/received/:replyId/download` | [docs](https://docs.notifyre.com/api/mms-received-download) |
| [Download Received Fax](actions/download-received-fax.md) | `GET /fax/received/:faxId/download` | [docs](https://docs.notifyre.com/api/fax-received-download) |
| [Download Sent Fax](actions/download-sent-fax.md) | `GET /fax/send/recipients/:recipientId/download` | [docs](https://docs.notifyre.com/api/fax-sent-download) |
| [Get Contact](actions/get-contact.md) | `GET /addressbook/contacts/:contactId` | [docs](https://docs.notifyre.com/api/address-book-contact) |
| [Get Fax Document Status](actions/get-fax-document-status.md) | `GET /fax/send/conversion/:fileName` | [docs](https://docs.notifyre.com/api/fax-document-status-get) |
| [Get Sent SMS](actions/get-sent-sms.md) | `GET /sms/send/:messageId` | [docs](https://docs.notifyre.com/api/sms-sent) |
| [Get Sent SMS Recipient](actions/get-sent-sms-recipient.md) | `GET /sms/send/:messageId/recipients/:recipientId` | [docs](https://docs.notifyre.com/api/sms-sent-recipient) |
| [Get SMS Reply](actions/get-sms-reply.md) | `GET /sms/received/:replyId` | [docs](https://docs.notifyre.com/api/sms-received) |
| [Get SMS Reply V2](actions/get-sms-reply-v2.md) | `GET /sms/received/:replyId/v2` | [docs](https://docs.notifyre.com/api/introduction) |
| [List Contacts](actions/list-contacts.md) | `POST /addressbook/contacts/search` | [docs](https://docs.notifyre.com/api/address-book-contacts-list) |
| [List Cover Pages](actions/list-cover-pages.md) | `GET /fax/coverpages` | [docs](https://docs.notifyre.com/api/fax-cover-pages) |
| [List Fax Numbers](actions/list-fax-numbers.md) | `GET /fax/numbers` | [docs](https://docs.notifyre.com/api/fax-numbers-list) |
| [List Fax Prices](actions/list-fax-prices.md) | `GET /fax/send/prices` | [docs](https://docs.notifyre.com/api/fax-send-prices) |
| [List Groups](actions/list-groups.md) | `GET /addressbook/groups` | [docs](https://docs.notifyre.com/api/address-book-groups-list) |
| [List Received Faxes](actions/list-received-faxes.md) | `GET /fax/received` | [docs](https://docs.notifyre.com/api/fax-received-list) |
| [List Sent Faxes](actions/list-sent-faxes.md) | `GET /fax/send` | [docs](https://docs.notifyre.com/api/fax-sent-list) |
| [List SMS Prices](actions/list-sms-prices.md) | `GET /sms/send/prices` | [docs](https://docs.notifyre.com/api/sms-send-prices) |
| [List SMS Replies](actions/list-sms-replies.md) | `GET /sms/received` | [docs](https://docs.notifyre.com/api/sms-received-list) |
| [Remove Contacts From Group](actions/remove-contacts-from-group.md) | `DELETE /addressbook/groups/contacts` | [docs](https://docs.notifyre.com/api/address-book-contacts-remove-from-group) |
| [Send Fax](actions/send-fax.md) | `POST /fax/send` | [docs](https://docs.notifyre.com/api/fax-send) |
| [Send SMS](actions/send-sms.md) | `POST /sms/send` | [docs](https://docs.notifyre.com/api/sms-send) |
| [Update Contact](actions/update-contact.md) | `PUT /addressbook/contacts/:contactId` | [docs](https://docs.notifyre.com/api/address-book-contact-update) |
| [Update Group](actions/update-group.md) | `PUT /addressbook/groups/:groupId` | [docs](https://docs.notifyre.com/api/address-book-group-update) |
| [Upload Fax Document](actions/upload-fax-document.md) | `POST /fax/send/conversion` | [docs](https://docs.notifyre.com/api/fax-document-upload) |
