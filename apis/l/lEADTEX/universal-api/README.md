# <img src="https://images.mindcloud.co/apps/icons/leadtex-icon_1776708760872.png" alt="LEADTEX logo" width="28" height="28"> LEADTEX: Universal API

LEADTEX chatbot constructor API for managing account information, messages, contacts, balances, tags, custom variables, lists, and media links.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lEADTEX/latest
- **Actions:** 51
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://leadteh.ru
- **Vendor API docs:** https://docs.leadteh.ru/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (51)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your current LEADTEX account details. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Contact](actions/create-or-update-contact.md) | PUT | Creates or updates a contact in LEADTEX. |
| [Create Or Update Telegram Contact](actions/create-or-update-telegram-contact.md) | PUT | Creates or updates a Telegram contact in LEADTEX. |
| [Create Or Update VK Contact](actions/create-or-update-vk-contact.md) | PUT | Creates or updates a VK contact in LEADTEX. |
| [Create Or Update WhatsApp Contact](actions/create-or-update-whatsapp-contact.md) | PUT | Creates or updates a WhatsApp contact in LEADTEX. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your LEADTEX account. |
| [List Contacts With Details](actions/list-contacts-with-details.md) | GET | Retrieves contacts with related details from LEADTEX. |

### Contact Account

| Action | Method | Description |
| --- | --- | --- |
| [Add Funds To Contact Account](actions/add-funds-to-contact-account.md) | PUT | Updates a contact account balance in LEADTEX by adding funds. |
| [Create Contact Account](actions/create-contact-account.md) | POST | Creates an ISO 4217 contact account in LEADTEX. |
| [Delete Contact Account](actions/delete-contact-account.md) | DELETE | Deletes an ISO 4217 contact account from LEADTEX. |
| [List Contact Accounts](actions/list-contact-accounts.md) | GET | Retrieves ISO 4217 contact accounts from LEADTEX. |
| [Withdraw Funds From Contact Account](actions/withdraw-funds-from-contact-account.md) | PUT | Updates a contact account balance in LEADTEX by withdrawing funds. |

### Contact Crypto Account

| Action | Method | Description |
| --- | --- | --- |
| [Add Funds To Contact Crypto Account](actions/add-funds-to-contact-crypto-account.md) | PUT | Updates a free-form contact account in LEADTEX by adding funds. |
| [Create Contact Crypto Account](actions/create-contact-crypto-account.md) | POST | Creates a free-form contact account in LEADTEX. |
| [Delete Contact Crypto Account](actions/delete-contact-crypto-account.md) | DELETE | Deletes a free-form contact account from LEADTEX. |
| [List Contact Crypto Accounts](actions/list-contact-crypto-accounts.md) | GET | Retrieves free-form contact accounts from LEADTEX. |
| [Withdraw Funds From Contact Crypto Account](actions/withdraw-funds-from-contact-crypto-account.md) | PUT | Updates a free-form contact account in LEADTEX by withdrawing funds. |

### Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [Attach Tag To Contact](actions/attach-tag-to-contact.md) | POST | Attaches a tag to a contact in LEADTEX by name. |
| [Attach Tag To Contact By ID](actions/attach-tag-to-contact-by-id.md) | POST | Attaches a tag to a contact in LEADTEX by ID. |
| [Detach Tag From Contact](actions/detach-tag-from-contact.md) | DELETE | Deletes a tag from a contact in LEADTEX by name. |
| [Detach Tag From Contact By ID](actions/detach-tag-from-contact-by-id.md) | DELETE | Deletes a tag from a contact in LEADTEX by ID. |

### Contact Variable

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact Variable](actions/delete-contact-variable.md) | DELETE | Deletes a contact variable from LEADTEX by name. |
| [Delete Contact Variable By ID](actions/delete-contact-variable-by-id.md) | DELETE | Deletes a contact variable from LEADTEX by ID. |
| [List Contact Variables](actions/list-contact-variables.md) | GET | Retrieves custom variables for a specific contact in LEADTEX. |
| [Set Contact Variable](actions/set-contact-variable.md) | PUT | Creates or updates a contact variable in LEADTEX. |

### List Item

| Action | Method | Description |
| --- | --- | --- |
| [Add List Item](actions/add-list-item.md) | POST | Creates a new item in a LEADTEX list. |
| [Delete List Item](actions/delete-list-item.md) | DELETE | Deletes an existing item from a LEADTEX list. |
| [List List Items](actions/list-list-items.md) | GET | Retrieves list items from a LEADTEX list. |
| [Update List Item](actions/update-list-item.md) | PUT | Updates an existing item in a LEADTEX list. |

### List Schema

| Action | Method | Description |
| --- | --- | --- |
| [Create List Schema](actions/create-list-schema.md) | POST | Creates a new list schema in LEADTEX. |
| [Delete List Schema](actions/delete-list-schema.md) | DELETE | Deletes a list schema from LEADTEX. |
| [Get List Schema](actions/get-list-schema.md) | GET | Retrieves a specific list schema from LEADTEX. |
| [List List Schemas](actions/list-list-schemas.md) | GET | Retrieves list schemas from your LEADTEX account. |

### List Schema Field

| Action | Method | Description |
| --- | --- | --- |
| [Add List Schema Field](actions/add-list-schema-field.md) | POST | Creates a new field in a LEADTEX list schema. |
| [Delete List Schema Field](actions/delete-list-schema-field.md) | DELETE | Deletes a field from a LEADTEX list schema. |

### Media Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Uploaded File Link](actions/get-uploaded-file-link.md) | GET | Retrieves the original link for an uploaded media file in LEADTEX. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send File By External ID](actions/send-file-by-external-id.md) | POST | Sends a file message in LEADTEX by external contact ID. |
| [Send File To Contact](actions/send-file-to-contact.md) | POST | Sends a file message to a contact in LEADTEX. |
| [Send Image By External ID](actions/send-image-by-external-id.md) | POST | Sends an image message in LEADTEX by external contact ID. |
| [Send Image To Contact](actions/send-image-to-contact.md) | POST | Sends an image message to a contact in LEADTEX. |
| [Send Message By External ID](actions/send-message-by-external-id.md) | POST | Sends a text message in LEADTEX by external contact ID. |
| [Send Message To Contact](actions/send-message-to-contact.md) | POST | Sends a text message to a contact in LEADTEX. |

### Queued Message

| Action | Method | Description |
| --- | --- | --- |
| [Queue Text Message](actions/queue-text-message.md) | POST | Queues a text message by phone number in LEADTEX. |
| [Queue Text Message To Bitrix Contact](actions/queue-text-message-to-bitrix-contact.md) | POST | Queues a text message to a Bitrix contact in LEADTEX. |
| [Queue Text Message To Contact](actions/queue-text-message-to-contact.md) | POST | Queues a text message to a contact in LEADTEX. |

### Referral

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Referrals](actions/list-contact-referrals.md) | GET | Retrieves referrals for a specific contact in LEADTEX. |

### Referral Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Contact Referrals](actions/count-contact-referrals.md) | GET | Retrieves the total referrals in a contact's network in LEADTEX. |

### Referrer

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Referrers](actions/get-contact-referrers.md) | GET | Retrieves referrers for a specific contact in LEADTEX. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Bot Tags](actions/list-bot-tags.md) | GET | Retrieves tags for a specific bot in LEADTEX. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves tags for a specific contact in LEADTEX. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp Message](actions/send-whatsapp-message.md) | POST | Sends a WhatsApp message by phone number in LEADTEX. |

