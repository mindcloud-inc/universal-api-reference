# <img src="https://images.mindcloud.co/apps/icons/heymarket-sms_1773694396887.png" alt="Heymarket SMS logo" width="28" height="28"> Heymarket SMS: Universal API

Manage contacts, conversations, and messages in Heymarket

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/heymarketSMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.heymarket.com/
- **Vendor API docs:** https://heymarket.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Batch Create Contacts](actions/batch-create-contacts.md) | POST |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Get Contact Status](actions/get-contact-status.md) | GET |  |
| [List Contact Fields](actions/list-contact-fields.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Set Contact Status](actions/set-contact-status.md) | PUT |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Close Conversation](actions/close-conversation.md) | PUT |  |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |
| [Mark Conversation Read](actions/mark-conversation-read.md) | PUT |  |
| [Mark Conversation Unread](actions/mark-conversation-unread.md) | PUT |  |
| [Open Conversation](actions/open-conversation.md) | PUT |  |
| [Reassign Conversation](actions/reassign-conversation.md) | PUT |  |

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [List Inboxes](actions/list-inboxes.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation Message History](actions/get-conversation-message-history.md) | GET |  |
| [List Team Messages](actions/list-team-messages.md) | GET |  |
| [Send Message](actions/send-message.md) | POST |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST |  |
| [Get Schedule](actions/get-schedule.md) | GET |  |
| [Update Schedule](actions/update-schedule.md) | PUT |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [Update Template](actions/update-template.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET |  |

