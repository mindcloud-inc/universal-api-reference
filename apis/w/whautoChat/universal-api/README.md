# <img src="https://images.mindcloud.co/apps/icons/whauto-chat_1775663028790.png" alt="WhautoChat logo" width="28" height="28"> WhautoChat: Universal API

WhautoChat is an omnichannel messaging and automation platform for managing contacts, broadcasts, templates, webhooks, staff, workspaces, and channel messages through a shared REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whautoChat/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whauto.chat
- **Vendor API docs:** https://help.whauto.chat/cloud-version/integrations/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create a Broadcast](actions/create-a-broadcast.md) | POST | Creates a new broadcast in WhautoChat. |
| [Delete Broadcast by ID](actions/delete-broadcast-by-id.md) | DELETE | Deletes an existing broadcast from WhautoChat by ID. |
| [Get Broadcast by ID](actions/get-broadcast-by-id.md) | GET | Retrieves a broadcast from WhautoChat by ID. |
| [Get Broadcast Logs](actions/get-broadcast-logs.md) | GET | Retrieves broadcast logs from WhautoChat. |
| [List/Search Broadcasts](actions/list-search-broadcasts.md) | GET | Finds broadcasts in WhautoChat. |
| [Update Broadcast by ID](actions/update-broadcast-by-id.md) | PUT | Updates an existing broadcast in WhautoChat by ID. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags to Contact](actions/add-tags-to-contact.md) | PUT | Adds tags to a contact in WhautoChat. |
| [Create New Contact](actions/create-new-contact.md) | POST | Creates a new contact in WhautoChat. |
| [Delete Contact by ID](actions/delete-contact-by-id.md) | DELETE | Deletes an existing contact from WhautoChat by ID. |
| [Get Contact by ID](actions/get-contact-by-id.md) | GET | Retrieves a contact from WhautoChat by ID. |
| [Remove Tags from Contact](actions/remove-tags-from-contact.md) | PUT | Removes tags from a contact in WhautoChat. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in WhautoChat. |
| [Update Contact by ID](actions/update-contact-by-id.md) | PUT | Updates an existing contact in WhautoChat by ID. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Instagram Template Message](actions/send-instagram-template-message.md) | POST | Sends an Instagram template message from WhautoChat. |
| [Send Instagram Text Message](actions/send-instagram-text-message.md) | POST | Sends an Instagram text message from WhautoChat. |
| [Send Messenger Media Message](actions/send-messenger-media-message.md) | POST | Sends a Messenger media message from WhautoChat. |
| [Send Messenger Template Message](actions/send-messenger-template-message.md) | POST | Sends a Messenger template message from WhautoChat. |
| [Send Messenger Text Message](actions/send-messenger-text-message.md) | POST | Sends a Messenger text message from WhautoChat. |
| [Send Telegram Template Message](actions/send-telegram-template-message.md) | POST | Sends a Telegram template message from WhautoChat. |
| [Send WhatsApp Media Message](actions/send-whats-app-media-message.md) | POST | Sends a WhatsApp media message from WhautoChat. |
| [Send WhatsApp Template Message](actions/send-whats-app-template-message.md) | POST | Sends a WhatsApp template message from WhautoChat. |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | POST | Sends a WhatsApp text message from WhautoChat. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Create a Segment](actions/create-a-segment.md) | POST | Creates a new segment in WhautoChat. |
| [Delete Segment by ID](actions/delete-segment-by-id.md) | DELETE | Deletes an existing segment from WhautoChat by ID. |
| [Get Segment by ID](actions/get-segment-by-id.md) | GET | Retrieves a segment from WhautoChat by ID. |
| [List/Search Segments](actions/list-search-segments.md) | GET | Finds segments in WhautoChat. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create a Webhook](actions/create-a-webhook.md) | POST | Creates a new webhook in WhautoChat. |
| [Delete a Webhook](actions/delete-a-webhook.md) | DELETE | Deletes an existing webhook from WhautoChat. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from WhautoChat. |
| [Update a Webhook](actions/update-a-webhook.md) | PUT | Updates an existing webhook in WhautoChat. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create a Contact Tag](actions/create-a-contact-tag.md) | POST | Creates a new contact tag in WhautoChat. |
| [Get Contact Tag by ID](actions/get-contact-tag-by-id.md) | GET | Retrieves a contact tag from WhautoChat by ID. |
| [List/Search Contact Tags](actions/list-search-contact-tags.md) | GET | Finds contact tags in WhautoChat. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create WhatsApp Template](actions/create-whats-app-template.md) | POST | Creates a new WhatsApp template in WhautoChat. |
| [Get WhatsApp Template by ID](actions/get-whats-app-template-by-id.md) | GET | Retrieves a WhatsApp template from WhautoChat by ID. |
| [List WhatsApp Templates](actions/list-whats-app-templates.md) | GET | Retrieves WhatsApp templates from WhautoChat. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Staff by ID](actions/get-staff-by-id.md) | GET | Retrieves a staff member from WhautoChat by ID. |
| [List/Search Staff](actions/list-search-staff.md) | GET | Finds staff members in WhautoChat. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace by ID](actions/get-workspace-by-id.md) | GET | Retrieves a workspace from WhautoChat by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from WhautoChat. |

