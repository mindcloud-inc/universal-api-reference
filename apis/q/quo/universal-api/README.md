# <img src="https://images.mindcloud.co/apps/icons/quo_1773173316041.png" alt="Quo logo" width="28" height="28"> Quo: Universal API

Manage business calls, texts, contacts, and shared inboxes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quo/latest
- **Category:** Support / Contact Center
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.quo.com
- **Vendor API docs:** https://www.quo.com/docs/mdx/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Call By ID](actions/get-call-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-by-id?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Callrecording

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Recordings](actions/get-call-recordings.md) | GET | Retrieves recordings for a Quo call. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Get Call By ID](actions/get-call-by-id.md) | GET | Retrieves a call from Quo by ID. |
| [List Calls](actions/list-calls.md) | GET | Retrieves all existing calls from Quo. |

### Callsummary

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Summary](actions/get-call-summary.md) | GET | Retrieves a summary for a Quo call. |

### Calltranscript

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Transcript](actions/get-call-transcript.md) | GET | Retrieves a transcription for a Quo call. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Quo. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Quo. |
| [Get Contact By ID](actions/get-contact-by-id.md) | GET | Retrieves a contact from Quo by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contacts from Quo. |
| [Update Contact By ID](actions/update-contact-by-id.md) | PUT | Updates an existing contact in Quo. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves all existing conversations from Quo. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Custom Fields](actions/get-contact-custom-fields.md) | GET | Retrieves contact custom fields from Quo. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message By ID](actions/get-message-by-id.md) | GET | Retrieves a message from Quo by ID. |
| [Send Message](actions/send-message.md) | POST | Sends a text message in Quo. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves all messages from Quo. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone Number By ID](actions/get-phone-number-by-id.md) | GET | Retrieves a phone number from Quo by ID. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves all phone numbers from Quo. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User By ID](actions/get-user-by-id.md) | GET | Retrieves a user from Quo by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves all users from Quo. |

### Voicemail

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Voicemail](actions/get-call-voicemail.md) | GET | Retrieves a voicemail for a Quo call. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Call Summary Webhook](actions/create-call-summary-webhook.md) | POST | Creates a new webhook for Quo call summaries. |
| [Create Call Transcript Webhook](actions/create-call-transcript-webhook.md) | POST | Creates a new webhook for Quo call transcripts. |
| [Create Call Webhook](actions/create-call-webhook.md) | POST | Creates a new webhook for Quo calls. |
| [Create Message Webhook](actions/create-message-webhook.md) | POST | Creates a new webhook for Quo messages. |
| [Delete Webhook By ID](actions/delete-webhook-by-id.md) | DELETE | Deletes an existing webhook from Quo. |
| [Get Webhook By ID](actions/get-webhook-by-id.md) | GET | Retrieves a webhook from Quo by ID. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhooks from Quo. |

