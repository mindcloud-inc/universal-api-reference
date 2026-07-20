# Sender: Native API Reference

A consolidated summary of Sender's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.sender.net/
- **API base URL:** `https://api.sender.net/v2`

## Authentication

### API Key

Bearer token authentication for the Sender API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.sender.net/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.lastPage`. The current page number is read from `meta.currentPage`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber to Group](actions/add-subscriber-to-group.md) | `POST /subscribers/groups/:groupId` | [docs](https://api.sender.net/subscribers/add-group/) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://api.sender.net/campaigns/create-campaign/) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://api.sender.net/groups/create-group/) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /subscribers` | [docs](https://api.sender.net/subscribers/add-subscriber/) |
| [Create Transactional Campaign](actions/create-transactional-campaign.md) | `POST /transactional` | [docs](https://api.sender.net/transactional_campaigns/create/) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers` | [docs](https://api.sender.net/subscribers/delete-subscriber/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:id` | [docs](https://api.sender.net/campaigns/get-one/) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://api.sender.net/groups/get-group/) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:subscriberKey` | [docs](https://api.sender.net/subscribers/get-one/) |
| [Get Transactional Campaign](actions/get-transactional-campaign.md) | `GET /transactional/:id` | [docs](https://api.sender.net/transactional_campaigns/get-one/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://api.sender.net/campaigns/get-all/) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://api.sender.net/fields/get-all/) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://api.sender.net/groups/list-all/) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://api.sender.net/segments/list-segments/) |
| [List Subscriber Events](actions/list-subscriber-events.md) | `GET /subscribers/:subscriberKey/events` | [docs](https://api.sender.net/subscribers/events/) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://api.sender.net/subscribers/list-all/) |
| [List Subscribers in Group](actions/list-subscribers-in-group.md) | `GET /groups/:id/subscribers` | [docs](https://api.sender.net/groups/subscribers/) |
| [List Transactional Campaigns](actions/list-transactional-campaigns.md) | `GET /transactional` | [docs](https://api.sender.net/transactional_campaigns/get-all/) |
| [Remove Subscriber from Group](actions/remove-subscriber-from-group.md) | `DELETE /subscribers/groups/:groupId` | [docs](https://api.sender.net/subscribers/remove-group/) |
| [Rename Group](actions/rename-group.md) | `PATCH /groups/:id` | [docs](https://api.sender.net/groups/update-group/) |
| [Schedule Send](actions/schedule-send.md) | `POST /campaigns/:id/schedule` | [docs](https://api.sender.net/campaigns/schedule-send/) |
| [Send Campaign](actions/send-campaign.md) | `POST /campaigns/:id/send` | [docs](https://api.sender.net/campaigns/send/) |
| [Send Transactional Email Without Template](actions/send-transactional-email-without-template.md) | `POST /message/send` | [docs](https://api.sender.net/transactional_campaigns/send-transactional/) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /subscribers/:subscriberKey` | [docs](https://api.sender.net/subscribers/update-subscriber/) |
