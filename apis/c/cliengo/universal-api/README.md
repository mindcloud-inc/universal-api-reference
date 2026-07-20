# <img src="https://images.mindcloud.co/apps/icons/cliengo_1773760207591.png" alt="Cliengo logo" width="28" height="28"> Cliengo: Universal API

Manage sites, contacts, chatbots, and customer conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cliengo/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cliengo.com
- **Vendor API docs:** https://developers.cliengo.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact History](actions/get-contact-history.md) | GET |  |

### Chatbot

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Chatbot](actions/get-site-chatbot.md) | GET |  |
| [List Chatbots](actions/list-chatbots.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Tags](actions/add-contact-tags.md) | PUT |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |
| [Update Contact Status](actions/update-contact-status.md) | PUT |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Count Site Conversations](actions/count-site-conversations.md) | GET |  |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Message](actions/create-contact-message.md) | POST |  |
| [List Contact Messages](actions/list-contact-messages.md) | GET |  |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST |  |
| [List Contact Notes](actions/list-contact-notes.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

