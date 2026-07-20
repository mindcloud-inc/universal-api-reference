# Watbot: Native API Reference

A consolidated summary of Watbot's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.watbot.ru
- **API base URL:** `https://watbot.ru/api/v1`

## Authentication

### API Key

Authenticate with a Watbot API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.watbot.ru/rabota-s-api/akkaunt)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `count` in the query string to set the page size (maximum 500). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Funds To Contact Account](actions/add-funds-to-contact-account.md) | `POST /addFundsToContactAccount` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/bills) |
| [Add List Item](actions/add-list-item.md) | `POST /addListItem` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska) |
| [Add List Schema Field](actions/add-list-schema-field.md) | `POST /addListSchemaField` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/spiski) |
| [Attach Tag To Contact](actions/attach-tag-to-contact.md) | `POST /attachTagToContact` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/tegi) |
| [Count Referral Network](actions/count-referral-network.md) | `POST /getCountReferrals` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/referalnaya-sistema) |
| [Create Contact Account](actions/create-contact-account.md) | `POST /addContactAccount` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/bills) |
| [Create List Schema](actions/create-list-schema.md) | `POST /createListSchema` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/spiski) |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /createOrUpdateContact` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty) |
| [Decode Media Short Link](actions/decode-media-short-link.md) | `POST /decodeShortLink` | [docs](https://docs.watbot.ru/rabota-s-api/ssylki-na-mediafaily) |
| [Delete Contact Account](actions/delete-contact-account.md) | `POST /deleteContactAccount` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/bills) |
| [Delete Contact Variable](actions/delete-contact-variable.md) | `POST /deleteContactVariable` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/polzovatelskie-peremennye) |
| [Delete List Item](actions/delete-list-item.md) | `POST /deleteListItem` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska) |
| [Delete List Schema](actions/delete-list-schema.md) | `POST /deleteListSchema` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/spiski) |
| [Delete List Schema Field](actions/delete-list-schema-field.md) | `POST /deleteListSchemaField` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/spiski) |
| [Detach Tag From Contact](actions/detach-tag-from-contact.md) | `POST /detachTagFromContact` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/tegi) |
| [Get Current Account](actions/get-current-account.md) | `GET /getMe` | [docs](https://docs.watbot.ru/rabota-s-api/akkaunt) |
| [Get List Schema](actions/get-list-schema.md) | `GET /getListSchema` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/spiski) |
| [List Bot Tags](actions/list-bot-tags.md) | `GET /getBotTags` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/tegi) |
| [List Contact Accounts](actions/list-contact-accounts.md) | `GET /getContactAccounts` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/bills) |
| [List Contact Referrals](actions/list-contact-referrals.md) | `POST /getReferrals` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/referalnaya-sistema) |
| [List Contact Referrers](actions/list-contact-referrers.md) | `GET /getReferrers` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/referalnaya-sistema) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /getContactTags` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/tegi) |
| [List Contact Variables](actions/list-contact-variables.md) | `GET /getContactVariables` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/polzovatelskie-peremennye) |
| [List Contacts](actions/list-contacts.md) | `GET /getContacts` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty) |
| [List List Items](actions/list-list-items.md) | `POST /getListItems` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska) |
| [List List Schemas](actions/list-list-schemas.md) | `GET /getListSchemas` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/spiski) |
| [Queue Broadcast Message](actions/queue-broadcast-message.md) | `POST /sendMessageToQueue` | [docs](https://docs.watbot.ru/rabota-s-api/rassylka) |
| [Send Message By External ID](actions/send-message-by-external-id.md) | `POST /sendMessage` | [docs](https://docs.watbot.ru/rabota-s-api/otpravit-soobshenie) |
| [Send Message To Contact](actions/send-message-to-contact.md) | `POST /sendMessage` | [docs](https://docs.watbot.ru/rabota-s-api/otpravit-soobshenie) |
| [Send Message To WhatsApp](actions/send-message-to-whats-app.md) | `POST /sendMessageToWhatsApp` | [docs](https://docs.watbot.ru/rabota-s-api/otpravit-soobshenie) |
| [Set Contact Variable](actions/set-contact-variable.md) | `POST /setContactVariable` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/polzovatelskie-peremennye) |
| [Set Ysell Status](actions/set-ysell-status.md) | `POST /setYsellStatus` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty) |
| [Update List Item](actions/update-list-item.md) | `POST /updateListItem` | [docs](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska) |
| [Withdraw Funds From Contact Account](actions/withdraw-funds-from-contact-account.md) | `POST /withdrawFundsFromContactAccount` | [docs](https://docs.watbot.ru/rabota-s-api/kontakty/bills) |
