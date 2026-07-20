# <img src="https://images.mindcloud.co/apps/icons/blooio-messaging_1775857134313.png" alt="Blooio Messaging logo" width="28" height="28"> Blooio Messaging: Universal API

Send and manage iMessage and SMS with Blooio's API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blooioMessaging/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://blooio.com
- **Vendor API docs:** https://docs.blooio.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Authentication Context](actions/get-current-authentication-context.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-current-authentication-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Tags](actions/add-contact-tags.md) | PUT | Adds tags to a contact in Blooio Messaging. |
| [Check Contact Capabilities](actions/check-contact-capabilities.md) | GET | Retrieves contact capabilities from Blooio Messaging. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Blooio Messaging. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Blooio Messaging. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Blooio Messaging. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves contact tags from Blooio Messaging. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Blooio Messaging. |
| [Remove Contact Tag](actions/remove-contact-tag.md) | DELETE | Removes a tag from a contact in Blooio Messaging. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Blooio Messaging. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Blooio Messaging. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes a group from Blooio Messaging. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Blooio Messaging. |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves group members from Blooio Messaging. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Blooio Messaging. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Blooio Messaging. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Blooio Messaging. |
| [Get Message Status](actions/get-message-status.md) | GET | Retrieves a message status from Blooio Messaging. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves messages from a Blooio Messaging chat. |
| [Send Message](actions/send-message.md) | POST | Sends a message in a Blooio Messaging chat. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [List Numbers](actions/list-numbers.md) | GET | Retrieves numbers from Blooio Messaging. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Authentication Context](actions/get-current-authentication-context.md) | GET | Retrieves the current authentication context from Blooio Messaging. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Blooio Messaging. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Blooio Messaging. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Blooio Messaging. |

