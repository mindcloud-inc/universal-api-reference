# WhautoChat: Native API Reference

A consolidated summary of WhautoChat's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://help.whauto.chat/cloud-version/integrations/rest-api/
- **API base URL:** `https://api.whauto.chat`

## Authentication

### API Key

Authenticate WhautoChat requests with an API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://help.whauto.chat/cloud-version/integrations/rest-api/)

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tags to Contact](actions/add-tags-to-contact.md) | `POST /v1/contacts/{contactId}/tags/add` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#6-add-tags-to-contact) |
| [Create a Broadcast](actions/create-a-broadcast.md) | `POST /v1/broadcasts` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#2-create-a-broadcast) |
| [Create a Contact Tag](actions/create-a-contact-tag.md) | `POST /v1/contactTags` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contact-tag/#2-create-a-contact-tag) |
| [Create a Segment](actions/create-a-segment.md) | `POST /v1/segments` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/segment/#2-create-a-segment) |
| [Create a Webhook](actions/create-a-webhook.md) | `POST /v1/webhooks` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/webhooks/#2-create-a-webhook) |
| [Create New Contact](actions/create-new-contact.md) | `POST /v1/contacts` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#2-create-new-contact) |
| [Create WhatsApp Template](actions/create-whats-app-template.md) | `POST /v1/whatsapp-template` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/whatsapp-templates/#3-create-whatsapp-template) |
| [Delete a Webhook](actions/delete-a-webhook.md) | `DELETE /v1/webhooks/{webhookId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/webhooks/#4-delete-a-webhook) |
| [Delete Broadcast by ID](actions/delete-broadcast-by-id.md) | `DELETE /v1/broadcasts/{broadcastId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#5-delete-broadcast-by-id) |
| [Delete Contact by ID](actions/delete-contact-by-id.md) | `DELETE /v1/contacts/{contactId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#5-delete-contact-by-id) |
| [Delete Segment by ID](actions/delete-segment-by-id.md) | `DELETE /v1/segments/{segmentId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/segment/#4-delete-segment-by-id) |
| [Get Broadcast by ID](actions/get-broadcast-by-id.md) | `GET /v1/broadcasts/{broadcastId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#3-get-broadcast-by-id) |
| [Get Broadcast Logs](actions/get-broadcast-logs.md) | `GET /v1/broadcasts/{broadcastId}/logs` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#6-get-broadcast-logs) |
| [Get Contact by ID](actions/get-contact-by-id.md) | `GET /v1/contacts/{contactId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#3-get-contact-by-id) |
| [Get Contact Tag by ID](actions/get-contact-tag-by-id.md) | `GET /v1/contactTags/{contactTagId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contact-tag/#3-get-contact-tag-by-id) |
| [Get Segment by ID](actions/get-segment-by-id.md) | `GET /v1/segments/{segmentId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/segment/#3-get-segment-by-id) |
| [Get Staff by ID](actions/get-staff-by-id.md) | `GET /v1/staffs/{staffId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/staff/#2-get-staff-by-id) |
| [Get WhatsApp Template by ID](actions/get-whats-app-template-by-id.md) | `GET /v1/whatsapp-templates/{templateId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/whatsapp-templates/#2-get-whatsapp-template-by-id) |
| [Get Workspace by ID](actions/get-workspace-by-id.md) | `GET /v1/workspaces/{workspaceId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/workspace/#2-get-workspace-by-id) |
| [List/Search Broadcasts](actions/list-search-broadcasts.md) | `GET /v1/broadcasts` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#1-listsearch-broadcasts) |
| [List/Search Contact Tags](actions/list-search-contact-tags.md) | `GET /v1/contactTags` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contact-tag/#1-listsearch-contact-tags) |
| [List/Search Segments](actions/list-search-segments.md) | `GET /v1/segments` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/segment/#1-listsearch-segments) |
| [List/Search Staff](actions/list-search-staff.md) | `GET /v1/staffs` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/staff/#1-listsearch-staff) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/webhooks/#1-list-webhooks) |
| [List WhatsApp Templates](actions/list-whats-app-templates.md) | `GET /v1/whatsapp-templates` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/whatsapp-templates/#1-list-whatsapp-templates) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/workspace/#1-list-workspaces) |
| [Remove Tags from Contact](actions/remove-tags-from-contact.md) | `POST /v1/contacts/{contactId}/tags/remove` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#7-remove-tags-from-contact) |
| [Search Contacts](actions/search-contacts.md) | `GET /v1/contacts` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#1-search-contacts) |
| [Send Instagram Template Message](actions/send-instagram-template-message.md) | `POST /v1/messages/instagram/sendtemplate` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#8-send-instagram-template-message) |
| [Send Instagram Text Message](actions/send-instagram-text-message.md) | `POST /v1/messages/instagram/sendtext` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#7-send-instagram-text-message) |
| [Send Messenger Media Message](actions/send-messenger-media-message.md) | `POST /v1/messages/messenger/sendmedia` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#5-send-messenger-media-message) |
| [Send Messenger Template Message](actions/send-messenger-template-message.md) | `POST /v1/messages/messenger/sendtemplate` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#6-send-messenger-template-message) |
| [Send Messenger Text Message](actions/send-messenger-text-message.md) | `POST /v1/messages/messenger/sendtext` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#4-send-messenger-text-message) |
| [Send Telegram Template Message](actions/send-telegram-template-message.md) | `POST /v1/messages/telegram/sendtemplate` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#9-send-telegram-template-message) |
| [Send WhatsApp Media Message](actions/send-whats-app-media-message.md) | `POST /v1/messages/whatsapp/sendmedia` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#2-send-whatsapp-media-message) |
| [Send WhatsApp Template Message](actions/send-whats-app-template-message.md) | `POST /v1/messages/whatsapp/sendtemplate` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#3-send-whatsapp-template-message) |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | `POST /v1/messages/whatsapp/sendtext` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#1-send-whatsapp-text-message) |
| [Update a Webhook](actions/update-a-webhook.md) | `PUT /v1/webhooks/{webhookId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/webhooks/#3-update-a-webhook) |
| [Update Broadcast by ID](actions/update-broadcast-by-id.md) | `PUT /v1/broadcasts/{broadcastId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#4-update-broadcast-by-id) |
| [Update Contact by ID](actions/update-contact-by-id.md) | `PUT /v1/contacts/{contactId}` | [docs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/contacts/#4-update-contact-by-id) |
