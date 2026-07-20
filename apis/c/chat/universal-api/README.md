# <img src="https://images.mindcloud.co/apps/icons/chat_1773759485071.png" alt="2Chat logo" width="28" height="28"> 2Chat: Universal API

Manage WhatsApp channels, contacts, messages, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chat/latest
- **Category:** Communication / Team Messaging
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://2chat.co
- **Vendor API docs:** https://developers.2chat.co/docs/category/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves your account details from 2Chat. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in 2Chat. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from 2Chat. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from 2Chat. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from 2Chat. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in 2Chat by search query. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in 2Chat. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves WhatsApp conversations from 2Chat for a channel. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Participant](actions/add-participant.md) | PUT | Updates a WhatsApp group in 2Chat by adding participants. |
| [Create Group](actions/create-group.md) | POST | Creates a WhatsApp group in 2Chat. |
| [List Group Participants](actions/list-group-participants.md) | GET | Retrieves WhatsApp group participants from 2Chat. |
| [List WhatsApp Groups](actions/list-whats-app-groups.md) | GET | Retrieves WhatsApp groups from 2Chat. |
| [Remove Participant](actions/remove-participant.md) | PUT | Updates a WhatsApp group in 2Chat by removing participants. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a WhatsApp message from 2Chat. |
| [Get a Message](actions/get-a-message.md) | GET | Retrieves a WhatsApp message from 2Chat. |
| [Get Messages by Phone Number](actions/get-messages-by-phone-number.md) | GET | Retrieves WhatsApp messages in 2Chat by phone number. |
| [Send WhatsApp Message](actions/send-whats-app-message.md) | POST | Creates a WhatsApp message in 2Chat. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List All Webhooks](actions/list-all-webhooks.md) | GET | Retrieves all webhook subscriptions from 2Chat. |
| [List Webhooks By Channel](actions/list-webhooks-by-channel.md) | GET | Retrieves webhook subscriptions for a 2Chat channel. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Check If Number Is On WhatsApp](actions/check-if-number-is-on-whats-app.md) | GET | Finds whether a phone number is on WhatsApp in 2Chat. |
| [Create WhatsApp QR Connection](actions/create-whats-app-qr-connection.md) | POST | Creates a WhatsApp QR connection in 2Chat. |
| [Execute Channel Command](actions/execute-channel-command.md) | PUT | Updates a WhatsApp channel in 2Chat with a command. |
| [Get Channel Status](actions/get-channel-status.md) | GET | Retrieves a WhatsApp channel status from 2Chat. |
| [Get WhatsApp Number](actions/get-whats-app-number.md) | GET | Retrieves a WhatsApp number from 2Chat. |
| [List WhatsApp Numbers](actions/list-whats-app-numbers.md) | GET | Retrieves connected WhatsApp numbers from 2Chat. |

