# Umbler Talk: Native API Reference

A consolidated summary of Umbler Talk's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://app-utalk.umbler.com/api/docs/index.html
- **OpenAPI specification:** https://app-utalk.umbler.com/api/docs/v1/docs.json
- **API base URL:** `https://app-utalk.umbler.com/api`

## Authentication

### API Key

Umbler Talk uses HTTP Bearer authentication. Paste only the generated token value into the API Key field; the connector supplies the Bearer authorization format.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app-utalk.umbler.com/api/docs/index.html)

## API conventions

Responses from this API use JSON.

## Pagination

Use `Take` in the query string to set the page size (default 50; minimum 1). Use `Skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `OrderBy` in the query string. Set the direction separately with `Order`. Use `Asc` for ascending order and `Desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | `POST /v1/chats/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Create Contact Note](actions/create-contact-note.md) | `POST /v1/contacts/[:id]/notes/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Create Message Reaction](actions/create-message-reaction.md) | `POST /v1/messages/reactions/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Create Quick Answer](actions/create-quick-answer.md) | `POST /v1/quick-answers/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Create Tag](actions/create-tag.md) | `POST /v1/tags/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Delete Contact Note](actions/delete-contact-note.md) | `DELETE /v1/contacts/[:id]/notes/[:noteId]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Edit Message](actions/edit-message.md) | `PUT /v1/messages/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Forward Message](actions/forward-message.md) | `POST /v1/messages/[:id]/forward/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Channel](actions/get-channel.md) | `GET /v1/channels/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Chat](actions/get-chat.md) | `GET /v1/chats/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | `GET /v1/contacts/phone/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Contact Note](actions/get-contact-note.md) | `GET /v1/contacts/[:id]/note/[:noteId]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Contact Profile](actions/get-contact-profile.md) | `GET /v1/contacts/[:id]/profile/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Current Member](actions/get-current-member.md) | `GET /v1/members/me/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Message](actions/get-message.md) | `GET /v1/messages/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Organization](actions/get-organization.md) | `GET /v1/organizations/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Organization Credits](actions/get-organization-credits.md) | `GET /v1/organizations/[:id]/credits/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Organization Details](actions/get-organization-details.md) | `GET /v1/organizations/[:id]/details/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Get Tag](actions/get-tag.md) | `GET /v1/tags/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Channels](actions/list-channels.md) | `GET /v1/channels/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Chat Favorite Messages](actions/list-chat-favorite-messages.md) | `GET /v1/chats/[:id]/favorite-messages/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Chat Relative Messages](actions/list-chat-relative-messages.md) | `GET /v1/chats/[:chatId]/relative-messages/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Chats](actions/list-chats.md) | `GET /v1/chats/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Contact Chats](actions/list-contact-chats.md) | `GET /v1/contacts/[:id]/chats/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /v1/contacts/[:id]/notes/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Message States](actions/list-message-states.md) | `GET /v1/messages/[:id]/states/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Online Members](actions/list-online-members.md) | `GET /v1/members/online/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Quick Answers](actions/list-quick-answers.md) | `GET /v1/quick-answers/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Sectors](actions/list-sectors.md) | `GET /v1/sectors/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [List Tags](actions/list-tags.md) | `GET /v1/tags/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Mark Chat Read](actions/mark-chat-read.md) | `PUT /v1/chats/[:id]/read/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Mark Chat Unread](actions/mark-chat-unread.md) | `PUT /v1/chats/[:id]/unread/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Send Message](actions/send-message.md) | `POST /v1/messages/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Send Simplified Message](actions/send-simplified-message.md) | `POST /v1/messages/simplified/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Update Chat](actions/update-chat.md) | `PUT /v1/chats/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/contacts/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
| [Update Tag](actions/update-tag.md) | `PUT /v1/tags/[:id]/` | [docs](https://app-utalk.umbler.com/api/docs/index.html) |
