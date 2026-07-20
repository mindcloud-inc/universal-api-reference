# SmartrMail: Native API Reference

A consolidated summary of SmartrMail's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.smartrmail.com/en/collections/30284-api
- **API base URL:** `https://go.smartrmail.com/api/v1`

## Authentication

### API Token

Connect with a SmartrMail API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.smartrmail.com/en/articles/636534-api-overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscribers to List](actions/add-subscribers-to-list.md) | `POST /lists/:list_id/list_subscribers` | [docs](https://docs.smartrmail.com/en/articles/636615-list-subscribers) |
| [Create Subscriber List](actions/create-subscriber-list.md) | `POST /lists` | [docs](https://docs.smartrmail.com/en/articles/636612-manage-subscriber-lists) |
| [Delete Subscriber List](actions/delete-subscriber-list.md) | `DELETE /lists/:list_id` | [docs](https://docs.smartrmail.com/en/articles/636612-manage-subscriber-lists) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:email_or_phone_or_uid` | [docs](https://docs.smartrmail.com/en/articles/636619-manage-individual-subscribers) |
| [Get Subscriber List](actions/get-subscriber-list.md) | `GET /lists/:list_id` | [docs](https://docs.smartrmail.com/en/articles/636612-manage-subscriber-lists) |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | `GET /lists` | [docs](https://docs.smartrmail.com/en/articles/636612-manage-subscriber-lists) |
| [List Subscribers in List](actions/list-subscribers-in-list.md) | `GET /lists/:list_id/list_subscribers` | [docs](https://docs.smartrmail.com/en/articles/636615-list-subscribers) |
| [Remove Subscriber From List](actions/remove-subscriber-from-list.md) | `DELETE /lists/:list_id/list_subscribers/:email_or_phone_or_uid` | [docs](https://docs.smartrmail.com/en/articles/636615-list-subscribers) |
| [Resubscribe Subscriber](actions/resubscribe-subscriber.md) | `POST /subscribers/:email_or_phone_or_uid/resubscribe` | [docs](https://docs.smartrmail.com/en/articles/636619-manage-individual-subscribers) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /subscribers/:email_or_phone_or_uid/unsubscribe` | [docs](https://docs.smartrmail.com/en/articles/636619-manage-individual-subscribers) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /subscribers/:email_or_phone_or_uid` | [docs](https://docs.smartrmail.com/en/articles/636619-manage-individual-subscribers) |
| [Update Subscriber List](actions/update-subscriber-list.md) | `PUT /lists/:list_id` | [docs](https://docs.smartrmail.com/en/articles/636612-manage-subscriber-lists) |
