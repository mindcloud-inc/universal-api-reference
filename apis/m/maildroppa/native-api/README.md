# Maildroppa: Native API Reference

A consolidated summary of Maildroppa's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://api.maildroppa.com
- **API base URL:** `https://api.maildroppa.com`

## Authentication

### API Key

Authenticate with a Maildroppa API key sent in the X-API-Key header on every request.

### Credentials

- **API Key:** `apiKey` · required · Maildroppa API key from Settings > User Profile > API key.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.maildroppa.com)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber Tag By Email](actions/add-subscriber-tag-by-email.md) | `POST /subscribers/tags/by-email` | [docs](https://api.maildroppa.com) |
| [Add Subscriber Tag By ID](actions/add-subscriber-tag-by-id.md) | `POST /subscribers/tags/by-id` | [docs](https://api.maildroppa.com) |
| [Count Filtered Subscribers](actions/count-filtered-subscribers.md) | `POST /subscribers/filtered-count` | [docs](https://api.maildroppa.com) |
| [Count Subscribers](actions/count-subscribers.md) | `GET /subscribers/count` | [docs](https://api.maildroppa.com) |
| [Create Double Opt-In Subscriber](actions/create-double-opt-in-subscriber.md) | `POST /subscribers/opt-in` | [docs](https://api.maildroppa.com) |
| [Create Segment](actions/create-segment.md) | `POST /subscriber/segment` | [docs](https://api.maildroppa.com) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /subscribers` | [docs](https://api.maildroppa.com) |
| [Create Subscriber Field](actions/create-subscriber-field.md) | `POST /field-type` | [docs](https://api.maildroppa.com) |
| [Create Tag](actions/create-tag.md) | `POST /tag-type` | [docs](https://api.maildroppa.com) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /subscriber/segment/{subscriberSegmentId}` | [docs](https://api.maildroppa.com) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/{subscriberId}` | [docs](https://api.maildroppa.com) |
| [Delete Subscriber By Email](actions/delete-subscriber-by-email.md) | `DELETE /subscribers/by-email/{email}` | [docs](https://api.maildroppa.com) |
| [Delete Subscriber Field](actions/delete-subscriber-field.md) | `DELETE /field-type/{fieldTypeId}` | [docs](https://api.maildroppa.com) |
| [Delete Subscriber Field By Email](actions/delete-subscriber-field-by-email.md) | `DELETE /subscribers/fields/by-email/{email}/{fieldTypeId}` | [docs](https://api.maildroppa.com) |
| [Delete Subscriber Field By ID](actions/delete-subscriber-field-by-id.md) | `DELETE /subscribers/fields/by-id/{subscriberId}/{fieldTypeId}` | [docs](https://api.maildroppa.com) |
| [Delete Subscriber Tag By Email](actions/delete-subscriber-tag-by-email.md) | `DELETE /subscribers/tags/by-email/{email}/{tagTypeId}` | [docs](https://api.maildroppa.com) |
| [Delete Subscriber Tag By ID](actions/delete-subscriber-tag-by-id.md) | `DELETE /subscribers/tags/by-id/{subscriberId}/{tagTypeId}` | [docs](https://api.maildroppa.com) |
| [Delete Subscribers](actions/delete-subscribers.md) | `DELETE /subscribers` | [docs](https://api.maildroppa.com) |
| [Delete Subscribers By Status](actions/delete-subscribers-by-status.md) | `DELETE /subscribers/all` | [docs](https://api.maildroppa.com) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tag-type/{tagId}` | [docs](https://api.maildroppa.com) |
| [Get Segment](actions/get-segment.md) | `GET /subscriber/segment/{segmentId}` | [docs](https://api.maildroppa.com) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/{subscriberId}` | [docs](https://api.maildroppa.com) |
| [List Field Matchers](actions/list-field-matchers.md) | `GET /field-type/matchers` | [docs](https://api.maildroppa.com) |
| [List Filtered Subscribers](actions/list-filtered-subscribers.md) | `POST /subscribers/filtered` | [docs](https://api.maildroppa.com) |
| [List Segments](actions/list-segments.md) | `GET /subscriber/segment` | [docs](https://api.maildroppa.com) |
| [List Signup Forms](actions/list-signup-forms.md) | `GET /form-builder` | [docs](https://api.maildroppa.com) |
| [List Subscriber Fields](actions/list-subscriber-fields.md) | `GET /field-type` | [docs](https://api.maildroppa.com) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://api.maildroppa.com) |
| [List Tags](actions/list-tags.md) | `GET /tag-type` | [docs](https://api.maildroppa.com) |
| [Update Segment](actions/update-segment.md) | `PUT /subscriber/segment/{subscriberSegmentId}` | [docs](https://api.maildroppa.com) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /subscribers/{subscriberId}` | [docs](https://api.maildroppa.com) |
| [Update Subscriber Email](actions/update-subscriber-email.md) | `PUT /subscribers/email/{subscriberId}` | [docs](https://api.maildroppa.com) |
| [Update Subscriber Field](actions/update-subscriber-field.md) | `PUT /field-type` | [docs](https://api.maildroppa.com) |
| [Update Tag](actions/update-tag.md) | `PUT /tag-type` | [docs](https://api.maildroppa.com) |
| [Upsert Subscriber Field By Email](actions/upsert-subscriber-field-by-email.md) | `POST /subscribers/fields/by-email` | [docs](https://api.maildroppa.com) |
| [Upsert Subscriber Field By ID](actions/upsert-subscriber-field-by-id.md) | `POST /subscribers/fields/by-id` | [docs](https://api.maildroppa.com) |
