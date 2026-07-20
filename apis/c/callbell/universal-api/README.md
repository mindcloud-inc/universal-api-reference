# <img src="https://images.mindcloud.co/apps/icons/callbell_1773857736661.png" alt="Callbell logo" width="28" height="28"> Callbell: Universal API

Manage chats, contacts, channels, and WhatsApp messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callbell/latest
- **Category:** Communication / Team Messaging
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.callbell.eu
- **Vendor API docs:** https://docs.callbell.eu/api/reference/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Auth Me](actions/get-auth-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-auth-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a specific channel from Callbell. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels for the current Callbell account. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Callbell. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Close Contact Conversation](actions/close-contact-conversation.md) | PUT | Closes a contact conversation in Callbell. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Callbell. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Callbell. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a specific contact from Callbell. |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | GET | Retrieves a Callbell contact by phone number. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts for the current Callbell account. |
| [Open Contact Conversation](actions/open-contact-conversation.md) | PUT | Reopens a contact conversation in Callbell. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Callbell. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST | Creates a conversation note for a Callbell contact. |
| [Get Message Status](actions/get-message-status.md) | GET | Retrieves message status details from Callbell. |
| [List Contact Messages](actions/list-contact-messages.md) | GET | Retrieves messages for a specific Callbell contact. |
| [Send Message](actions/send-message.md) | POST | Creates a new outbound message in Callbell. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List Funnels](actions/list-funnels.md) | GET | Retrieves funnels for the current Callbell account. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Status](actions/create-custom-status.md) | POST | Creates a new custom status in Callbell. |
| [Delete Custom Status](actions/delete-custom-status.md) | DELETE | Deletes an existing custom status from Callbell. |
| [List Custom Statuses](actions/list-custom-statuses.md) | GET | Retrieves custom statuses for the current Callbell account. |
| [Update Custom Status](actions/update-custom-status.md) | PUT | Updates an existing custom status in Callbell. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET | Retrieves current account plan details from Callbell. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Me](actions/get-auth-me.md) | GET | Retrieves current authenticated user details from Callbell. |

