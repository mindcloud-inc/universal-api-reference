# LEADTEX: Native API Reference

A consolidated summary of LEADTEX's API configuration and 51 documented operations, with links to official documentation.

- **Official docs:** https://docs.leadteh.ru/
- **API base URL:** `https://app.leadteh.ru/api/v1`

## Authentication

### API token

Stores one LEADTEX API token and sends it as the api_token query parameter required by LEADTEX.

### Credentials

- **API token:** `apiKey` · required · LEADTEX API token. It is sent as the api_token query parameter on every request.

[Official authentication documentation](https://docs.leadteh.ru/rabota-s-api/osnovy/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts.

## Endpoints (51 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Funds To Contact Account](actions/add-funds-to-contact-account.md) | `POST /addFundsToContactAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/) |
| [Add Funds To Contact Crypto Account](actions/add-funds-to-contact-crypto-account.md) | `POST /addFundsToContactCryptoAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/) |
| [Add List Item](actions/add-list-item.md) | `POST /addListItem?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/) |
| [Add List Schema Field](actions/add-list-schema-field.md) | `POST /addListSchemaField?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/) |
| [Attach Tag To Contact](actions/attach-tag-to-contact.md) | `POST /attachTagToContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/) |
| [Attach Tag To Contact By ID](actions/attach-tag-to-contact-by-id.md) | `POST /attachTagToContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/) |
| [Count Contact Referrals](actions/count-contact-referrals.md) | `POST /getCountReferrals?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/referalnaya-sistema/) |
| [Create Contact Account](actions/create-contact-account.md) | `POST /addContactAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/) |
| [Create Contact Crypto Account](actions/create-contact-crypto-account.md) | `POST /addContactCryptoAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/) |
| [Create List Schema](actions/create-list-schema.md) | `POST /createListSchema?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/) |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /createOrUpdateContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/) |
| [Create Or Update Telegram Contact](actions/create-or-update-telegram-contact.md) | `POST /createOrUpdateContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/) |
| [Create Or Update VK Contact](actions/create-or-update-vk-contact.md) | `POST /createOrUpdateContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/) |
| [Create Or Update WhatsApp Contact](actions/create-or-update-whatsapp-contact.md) | `POST /createOrUpdateContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/) |
| [Delete Contact Account](actions/delete-contact-account.md) | `POST /deleteContactAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/) |
| [Delete Contact Crypto Account](actions/delete-contact-crypto-account.md) | `POST /deleteContactCryptoAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/) |
| [Delete Contact Variable](actions/delete-contact-variable.md) | `POST /deleteContactVariable?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/) |
| [Delete Contact Variable By ID](actions/delete-contact-variable-by-id.md) | `POST /deleteContactVariable?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/) |
| [Delete List Item](actions/delete-list-item.md) | `POST /deleteListItem?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/) |
| [Delete List Schema](actions/delete-list-schema.md) | `POST /deleteListSchema?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/) |
| [Delete List Schema Field](actions/delete-list-schema-field.md) | `POST /deleteListSchemaField?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/) |
| [Detach Tag From Contact](actions/detach-tag-from-contact.md) | `POST /detachTagFromContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/) |
| [Detach Tag From Contact By ID](actions/detach-tag-from-contact-by-id.md) | `POST /detachTagFromContact?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/) |
| [Get Account](actions/get-account.md) | `GET /getMe?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/akkaunt/) |
| [Get Contact Referrers](actions/get-contact-referrers.md) | `GET /getReferrers?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/referalnaya-sistema/) |
| [Get List Schema](actions/get-list-schema.md) | `GET /getListSchema?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/) |
| [Get Uploaded File Link](actions/get-uploaded-file-link.md) | `POST /decodeShortLink?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/dopolnitelnye-metody/ssylki-na-mediafaily/) |
| [List Bot Tags](actions/list-bot-tags.md) | `GET /getBotTags?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/) |
| [List Contact Accounts](actions/list-contact-accounts.md) | `GET /getContactAccounts?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/) |
| [List Contact Crypto Accounts](actions/list-contact-crypto-accounts.md) | `GET /getContactCryptoAccounts?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/) |
| [List Contact Referrals](actions/list-contact-referrals.md) | `POST /getReferrals?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/referalnaya-sistema/) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /getContactTags?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/) |
| [List Contact Variables](actions/list-contact-variables.md) | `GET /getContactVariables?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/) |
| [List Contacts](actions/list-contacts.md) | `GET /getContacts?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/) |
| [List Contacts With Details](actions/list-contacts-with-details.md) | `GET /getContacts?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/) |
| [List List Items](actions/list-list-items.md) | `POST /getListItems?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/) |
| [List List Schemas](actions/list-list-schemas.md) | `GET /getListSchemas?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/) |
| [Queue Text Message](actions/queue-text-message.md) | `POST /sendMessageToQueue?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/rassylka/) |
| [Queue Text Message To Bitrix Contact](actions/queue-text-message-to-bitrix-contact.md) | `POST /sendMessageToQueue?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/rassylka/) |
| [Queue Text Message To Contact](actions/queue-text-message-to-contact.md) | `POST /sendMessageToQueue?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/rassylka/) |
| [Send File By External ID](actions/send-file-by-external-id.md) | `POST /sendMessage?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/soobsheniya/) |
| [Send File To Contact](actions/send-file-to-contact.md) | `POST /sendMessage?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/soobsheniya/) |
| [Send Image By External ID](actions/send-image-by-external-id.md) | `POST /sendMessage?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/soobsheniya/) |
| [Send Image To Contact](actions/send-image-to-contact.md) | `POST /sendMessage?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/soobsheniya/) |
| [Send Message By External ID](actions/send-message-by-external-id.md) | `POST /sendMessage?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/soobsheniya/) |
| [Send Message To Contact](actions/send-message-to-contact.md) | `POST /sendMessage?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/soobsheniya/) |
| [Send WhatsApp Message](actions/send-whatsapp-message.md) | `POST /sendMessageToWhatsApp?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/soobsheniya/) |
| [Set Contact Variable](actions/set-contact-variable.md) | `POST /setContactVariable?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/polzovatelskie-peremennye/) |
| [Update List Item](actions/update-list-item.md) | `POST /updateListItem?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/) |
| [Withdraw Funds From Contact Account](actions/withdraw-funds-from-contact-account.md) | `POST /withdrawFundsFromContactAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/scheta/) |
| [Withdraw Funds From Contact Crypto Account](actions/withdraw-funds-from-contact-crypto-account.md) | `POST /withdrawFundsFromContactCryptoAccount?api_token={{credentials.apiKey}}` | [docs](https://docs.leadteh.ru/rabota-s-api/kontakty/svobodnye-scheta/) |
