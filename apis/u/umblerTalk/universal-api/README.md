# <img src="https://images.mindcloud.co/apps/icons/e49fc3997536ff05dd624448cb9d2aacfafb09c1_1776102707014.png" alt="Umbler Talk logo" width="28" height="28"> Umbler Talk: Universal API

Manage WhatsApp chats, contacts, messages, and support workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/umblerTalk/latest
- **Category:** Support / Contact Center
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.umbler.com/home
- **Vendor API docs:** https://app-utalk.umbler.com/api/docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Member](actions/get-current-member.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-current-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Umbler Talk. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from Umbler Talk. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | POST | Finds a chat in Umbler Talk, or creates one if needed. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from Umbler Talk. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from Umbler Talk. |
| [List Contact Chats](actions/list-contact-chats.md) | GET | Retrieves a contact's chats from Umbler Talk. |
| [Mark Chat Read](actions/mark-chat-read.md) | PUT | Marks a chat as read in Umbler Talk. |
| [Mark Chat Unread](actions/mark-chat-unread.md) | PUT | Marks a chat as unread in Umbler Talk. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in Umbler Talk. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Umbler Talk. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Umbler Talk. |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | GET | Finds a contact in Umbler Talk by phone number. |
| [Get Contact Profile](actions/get-contact-profile.md) | GET | Retrieves a contact profile from Umbler Talk. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Umbler Talk. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Umbler Talk. |

### Contact Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST | Creates a contact note in Umbler Talk. |
| [Delete Contact Note](actions/delete-contact-note.md) | DELETE | Deletes a contact note from Umbler Talk. |
| [Get Contact Note](actions/get-contact-note.md) | GET | Retrieves a contact note from Umbler Talk. |
| [List Contact Notes](actions/list-contact-notes.md) | GET | Retrieves a contact's notes from Umbler Talk. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Member](actions/get-current-member.md) | GET | Retrieves the current member profile from Umbler Talk. |
| [List Online Members](actions/list-online-members.md) | GET | Retrieves online members from Umbler Talk. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Edit Message](actions/edit-message.md) | PUT | Updates an existing message in Umbler Talk. |
| [Forward Message](actions/forward-message.md) | POST | Forwards a message in Umbler Talk. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Umbler Talk. |
| [List Chat Favorite Messages](actions/list-chat-favorite-messages.md) | GET | Retrieves a chat's favorite messages from Umbler Talk. |
| [List Chat Relative Messages](actions/list-chat-relative-messages.md) | GET | Retrieves chat messages around a selected date in Umbler Talk. |
| [Send Message](actions/send-message.md) | POST | Creates a message in Umbler Talk. |
| [Send Simplified Message](actions/send-simplified-message.md) | POST | Creates a simplified message in Umbler Talk. |

### Message Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Message Reaction](actions/create-message-reaction.md) | POST | Creates a message reaction in Umbler Talk. |

### Message State

| Action | Method | Description |
| --- | --- | --- |
| [List Message States](actions/list-message-states.md) | GET | Retrieves a message's state history from Umbler Talk. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization summary from Umbler Talk. |
| [Get Organization Credits](actions/get-organization-credits.md) | GET | Retrieves organization conversation limits from Umbler Talk. |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves organization details from Umbler Talk. |

### Quick Answer

| Action | Method | Description |
| --- | --- | --- |
| [Create Quick Answer](actions/create-quick-answer.md) | POST | Creates a new quick answer in Umbler Talk. |
| [List Quick Answers](actions/list-quick-answers.md) | GET | Retrieves quick answers from Umbler Talk. |

### Sector

| Action | Method | Description |
| --- | --- | --- |
| [List Sectors](actions/list-sectors.md) | GET | Retrieves sectors from Umbler Talk. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Umbler Talk. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Umbler Talk. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Umbler Talk. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Umbler Talk. |

