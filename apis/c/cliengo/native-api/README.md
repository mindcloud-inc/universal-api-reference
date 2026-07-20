# Cliengo: Native API Reference

A consolidated summary of Cliengo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.cliengo.com/reference
- **API base URL:** `https://api.cliengo.com/1.0`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **JWT:** `jwt` · optional · JWT obtained from Cliengo's /jwt endpoint using your API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.cliengo.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `paging.page`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Tags](actions/add-contact-tags.md) | `POST /contacts/:contactId/tags` | [docs](https://developers.cliengo.com/reference/contactscontactidtags) |
| [Count Site Conversations](actions/count-site-conversations.md) | `GET /conversations/:websiteId/count` | [docs](https://developers.cliengo.com/reference/conversations) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.cliengo.com/reference/contact) |
| [Create Contact Message](actions/create-contact-message.md) | `POST /contacts/:contactId/messages` | [docs](https://developers.cliengo.com/reference/contactscontactidmessages) |
| [Create Contact Note](actions/create-contact-note.md) | `POST /contacts/:contactId/notes` | [docs](https://developers.cliengo.com/reference/contactcontactidnotes-1) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://developers.cliengo.com/reference/conversations) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contactId` | [docs](https://developers.cliengo.com/reference/contactscontactid-1) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://developers.cliengo.com/reference/companiesinput) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://developers.cliengo.com/reference/contactid) |
| [Get Contact History](actions/get-contact-history.md) | `GET /contacts/:contactId/history` | [docs](https://developers.cliengo.com/reference/contactscontactidhistory) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:conversationId` | [docs](https://developers.cliengo.com/reference/conversations-getbyid) |
| [Get Site](actions/get-site.md) | `GET /sites/:id` | [docs](https://developers.cliengo.com/reference/websiteswebsiteid) |
| [Get Site Chatbot](actions/get-site-chatbot.md) | `GET /sites/:id/chatbot` | [docs](https://developers.cliengo.com/reference/chatbots) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://developers.cliengo.com/reference/usersuserid) |
| [List Chatbots](actions/list-chatbots.md) | `GET /sites/chatbots` | [docs](https://developers.cliengo.com/reference/chatbots) |
| [List Contact Messages](actions/list-contact-messages.md) | `GET /contacts/:contactId/messages` | [docs](https://developers.cliengo.com/reference/contactcontactidmessages) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /contacts/:contactId/notes` | [docs](https://developers.cliengo.com/reference/contactcontactidnotes) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.cliengo.com/reference/contacts-get) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /conversations/:conversationId/messages` | [docs](https://developers.cliengo.com/reference/conversations-id-messages-get) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://developers.cliengo.com/reference/conversations) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://developers.cliengo.com/reference/websites) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.cliengo.com/reference/users) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:contactId` | [docs](https://developers.cliengo.com/reference/contactscontactid) |
| [Update Contact Status](actions/update-contact-status.md) | `PUT /contacts/:contactId/status` | [docs](https://developers.cliengo.com/reference/contactscontactidstatus) |
