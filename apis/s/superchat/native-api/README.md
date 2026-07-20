# Superchat: Native API Reference

A consolidated summary of Superchat's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.superchat.com/reference/welcome
- **API base URL:** `https://api.superchat.com/v1.0`

## Authentication

### API Key

Authenticate Superchat requests with the workspace API token sent in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developers.superchat.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next_cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact to Contact List](actions/add-contact-to-contact-list.md) | `POST /contacts/{contact_id}/contact-lists` | [docs](https://developers.superchat.com/reference/createcontactlistsforcontact) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.superchat.com/reference/createcontact) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://developers.superchat.com/reference/createatemplate-1) |
| [Create Template Folder](actions/create-template-folder.md) | `POST /template-folders` | [docs](https://developers.superchat.com/reference/createtemplatefolder) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.superchat.com/reference/createwebhook) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{contact_id}` | [docs](https://developers.superchat.com/reference/deletecontact) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/{template_id}` | [docs](https://developers.superchat.com/reference/deletetemplate) |
| [Get Channel](actions/get-channel.md) | `GET /channels/{channel_id}` | [docs](https://developers.superchat.com/reference/getchannel) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{contact_id}` | [docs](https://developers.superchat.com/reference/getcontact) |
| [Get Contact List](actions/get-contact-list.md) | `GET /contact-lists/{contact_list_id}` | [docs](https://developers.superchat.com/reference/getcontactlist) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/{conversation_id}` | [docs](https://developers.superchat.com/reference/getconversation) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://developers.superchat.com/reference/getme) |
| [Get File](actions/get-file.md) | `GET /files/{file_id}` | [docs](https://developers.superchat.com/reference/getfile) |
| [Get Inbox](actions/get-inbox.md) | `GET /inboxes/{inbox_id}` | [docs](https://developers.superchat.com/reference/getinbox) |
| [Get Label](actions/get-label.md) | `GET /labels/{label_id}` | [docs](https://developers.superchat.com/reference/getlabel) |
| [Get Template](actions/get-template.md) | `GET /templates/{template_id}` | [docs](https://developers.superchat.com/reference/gettemplate) |
| [Get User](actions/get-user.md) | `GET /users/{user_id}` | [docs](https://developers.superchat.com/reference/getuser) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://developers.superchat.com/reference/listchannels) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contact-lists` | [docs](https://developers.superchat.com/reference/listcontactlists) |
| [List Contact Lists for Contact](actions/list-contact-lists-for-contact.md) | `GET /contacts/{contact_id}/contact-lists` | [docs](https://developers.superchat.com/reference/getcontactlistsfromcontact) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.superchat.com/reference/listcontacts) |
| [List Contacts for Contact List](actions/list-contacts-for-contact-list.md) | `GET /contact-lists/{contact_list_id}/contacts` | [docs](https://developers.superchat.com/reference/listcontactsforcontactlist) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://developers.superchat.com/reference/listconversations) |
| [List Conversations for Contact](actions/list-conversations-for-contact.md) | `GET /contacts/{contact_id}/conversations` | [docs](https://developers.superchat.com/reference/getconversationforcontact) |
| [List Custom Attributes](actions/list-custom-attributes.md) | `GET /custom-attributes` | [docs](https://developers.superchat.com/reference/listcontactattributes) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://developers.superchat.com/reference/listfiles) |
| [List Inboxes](actions/list-inboxes.md) | `GET /inboxes` | [docs](https://developers.superchat.com/reference/listinboxes) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://developers.superchat.com/reference/listlabels) |
| [List Template Folders](actions/list-template-folders.md) | `GET /template-folders` | [docs](https://developers.superchat.com/reference/listtemplatefolders) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.superchat.com/reference/listtemplates) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.superchat.com/reference/listusers) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.superchat.com/reference/listwebhooks) |
| [Search Contacts](actions/search-contacts.md) | `POST /contacts/search` | [docs](https://developers.superchat.com/reference/searchcontact) |
| [Send Message](actions/send-message.md) | `POST /messages` | [docs](https://developers.superchat.com/reference/createmessage) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{contact_id}` | [docs](https://developers.superchat.com/reference/updatecontact) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /conversations/{conversation_id}` | [docs](https://developers.superchat.com/reference/patchconversation) |
| [Update Template](actions/update-template.md) | `PATCH /templates/{template_id}` | [docs](https://developers.superchat.com/reference/updatetemplate) |
| [Update Template Folder](actions/update-template-folder.md) | `PUT /template-folders/{folder_id}` | [docs](https://developers.superchat.com/reference/updatetemplatefolder) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/{webhook_id}` | [docs](https://developers.superchat.com/reference/updatewebhook) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://developers.superchat.com/reference/createfile) |
