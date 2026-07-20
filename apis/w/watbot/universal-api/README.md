# <img src="https://images.mindcloud.co/apps/icons/watbot_1776458995892.png" alt="Watbot logo" width="28" height="28"> Watbot: Universal API

Build chatbots, manage contacts, and automate customer messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/watbot/latest
- **Category:** Communication / Team Messaging
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://watbot.ru
- **Vendor API docs:** https://docs.watbot.ru

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves current account details from Watbot. |

### Broadcast Message

| Action | Method | Description |
| --- | --- | --- |
| [Queue Broadcast Message](actions/queue-broadcast-message.md) | POST | Queues a broadcast message in Watbot. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Contact](actions/create-or-update-contact.md) | POST | Finds a contact in Watbot, or creates one if no match is found. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Watbot. |
| [Set Ysell Status](actions/set-ysell-status.md) | PUT | Updates a contact's Ysell status in Watbot. |

### Contact Account

| Action | Method | Description |
| --- | --- | --- |
| [Add Funds To Contact Account](actions/add-funds-to-contact-account.md) | PUT | Adds funds to a contact account in Watbot. |
| [Create Contact Account](actions/create-contact-account.md) | POST | Creates a new contact account in Watbot. |
| [Delete Contact Account](actions/delete-contact-account.md) | DELETE | Deletes an existing contact account from Watbot. |
| [List Contact Accounts](actions/list-contact-accounts.md) | GET | Retrieves contact accounts from Watbot. |
| [Withdraw Funds From Contact Account](actions/withdraw-funds-from-contact-account.md) | PUT | Withdraws funds from a contact account in Watbot. |

### Contact Variable

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact Variable](actions/delete-contact-variable.md) | DELETE | Deletes a contact variable from Watbot. |
| [List Contact Variables](actions/list-contact-variables.md) | GET | Retrieves contact variables from Watbot. |
| [Set Contact Variable](actions/set-contact-variable.md) | PUT | Sets a contact variable in Watbot. |

### List Item

| Action | Method | Description |
| --- | --- | --- |
| [Add List Item](actions/add-list-item.md) | POST | Creates a new list item in Watbot. |
| [Delete List Item](actions/delete-list-item.md) | DELETE | Deletes an existing list item from Watbot. |
| [List List Items](actions/list-list-items.md) | GET | Retrieves list items from a Watbot list schema. |
| [Update List Item](actions/update-list-item.md) | PUT | Updates an existing list item in Watbot. |

### List Schema

| Action | Method | Description |
| --- | --- | --- |
| [Create List Schema](actions/create-list-schema.md) | POST | Creates a new list schema in Watbot. |
| [Delete List Schema](actions/delete-list-schema.md) | DELETE | Deletes an existing list schema from Watbot. |
| [Get List Schema](actions/get-list-schema.md) | GET | Retrieves a list schema from Watbot. |
| [List List Schemas](actions/list-list-schemas.md) | GET | Retrieves list schemas from Watbot. |

### List Schema Field

| Action | Method | Description |
| --- | --- | --- |
| [Add List Schema Field](actions/add-list-schema-field.md) | PUT | Adds a field to a list schema in Watbot. |
| [Delete List Schema Field](actions/delete-list-schema-field.md) | DELETE | Deletes a list schema field from Watbot. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [Decode Media Short Link](actions/decode-media-short-link.md) | GET | Decodes a media short link in Watbot. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message By External ID](actions/send-message-by-external-id.md) | POST | Creates a new message in Watbot by external contact ID. |
| [Send Message To Contact](actions/send-message-to-contact.md) | POST | Creates a new message for a Watbot contact. |

### Referral

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Referrals](actions/list-contact-referrals.md) | GET | Retrieves referrals for a Watbot contact. |

### Referral Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Referral Network](actions/count-referral-network.md) | GET | Retrieves referral network counts for a Watbot contact. |

### Referrer

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Referrers](actions/list-contact-referrers.md) | GET | Retrieves referrers for a Watbot contact. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Attach Tag To Contact](actions/attach-tag-to-contact.md) | PUT | Attaches a tag to a contact in Watbot. |
| [Detach Tag From Contact](actions/detach-tag-from-contact.md) | DELETE | Detaches a tag from a contact in Watbot. |
| [List Bot Tags](actions/list-bot-tags.md) | GET | Retrieves bot tags from Watbot. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves contact tags from Watbot. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message To WhatsApp](actions/send-message-to-whats-app.md) | POST | Creates a new WhatsApp message in Watbot. |

