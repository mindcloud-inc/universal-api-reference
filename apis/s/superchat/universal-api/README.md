# <img src="https://images.mindcloud.co/apps/icons/superchat_1774453365208.png" alt="Superchat logo" width="28" height="28"> Superchat: Universal API

Manage contacts, conversations, templates, files, and multichannel messages in Superchat.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/superchat/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://superchat.com
- **Vendor API docs:** https://developers.superchat.com/reference/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Superchat by ID. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from a Superchat workspace. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Superchat. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Superchat. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Superchat by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Superchat workspace. |
| [List Contacts for Contact List](actions/list-contacts-for-contact-list.md) | GET | Retrieves contacts for a Superchat contact list. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Superchat by any field. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Superchat. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact to Contact List](actions/add-contact-to-contact-list.md) | POST | Adds a contact to a Superchat contact list. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from Superchat by ID. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from a Superchat workspace. |
| [List Contact Lists for Contact](actions/list-contact-lists-for-contact.md) | GET | Retrieves contact lists for a Superchat contact. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Superchat by ID. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from a Superchat workspace. |
| [List Conversations for Contact](actions/list-conversations-for-contact.md) | GET | Retrieves conversations for a Superchat contact. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Superchat. |

### Custom Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Attributes](actions/list-custom-attributes.md) | GET | Retrieves custom contact attributes from Superchat. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Superchat by ID. |
| [List Files](actions/list-files.md) | GET | Retrieves files from a Superchat workspace. |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Superchat. |

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbox](actions/get-inbox.md) | GET | Retrieves an inbox from Superchat by ID. |
| [List Inboxes](actions/list-inboxes.md) | GET | Retrieves inboxes from a Superchat workspace. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from Superchat by ID. |
| [List Labels](actions/list-labels.md) | GET | Retrieves all conversation labels from Superchat. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Sends a message to a contact in Superchat. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Superchat. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Superchat. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Superchat by ID. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from a Superchat workspace. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Superchat. |

### Template Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Folder](actions/create-template-folder.md) | POST | Creates a new template folder in Superchat. |
| [List Template Folders](actions/list-template-folders.md) | GET | Retrieves all template folders from Superchat. |
| [Update Template Folder](actions/update-template-folder.md) | PUT | Updates an existing template folder in Superchat. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves current user details from Superchat. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Superchat by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a Superchat workspace. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Superchat. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from a Superchat workspace. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Superchat. |

