# Request Tracker (RT): Native API Reference

A consolidated summary of Request Tracker (RT)'s API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html
- **API base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`

## Authentication

### API Token

Use an RT auth token to access the REST2 API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.bestpractical.com/rt/6.0.2/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `order`. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Comment on Ticket](actions/comment-on-ticket.md) | `POST ticket/:ticketId/comment` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Correspond on Ticket](actions/correspond-on-ticket.md) | `POST ticket/:ticketId/correspond` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Create Queue](actions/create-queue.md) | `POST queue` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues) |
| [Create Ticket](actions/create-ticket.md) | `POST ticket` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Create User](actions/create-user.md) | `POST user` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Users) |
| [Get Group](actions/get-group.md) | `GET group/:groupId` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Groups) |
| [Get Group Members](actions/get-group-members.md) | `GET group/:groupId/members` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Group-Members) |
| [Get Queue](actions/get-queue.md) | `GET queue/:queueId` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues) |
| [Get Ticket](actions/get-ticket.md) | `GET ticket/:ticketId` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Get Ticket Attachments](actions/get-ticket-attachments.md) | `GET ticket/:ticketId/attachments` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Attachments-and-Messages) |
| [Get Ticket History](actions/get-ticket-history.md) | `GET ticket/:ticketId/history` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Transactions) |
| [Get User](actions/get-user.md) | `GET user/:userId` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Users) |
| [Get User Groups](actions/get-user-groups.md) | `GET user/:userId/groups` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#User-Memberships) |
| [List Queues](actions/list-queues.md) | `GET queues/all` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues) |
| [Search Groups](actions/search-groups.md) | `GET groups` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Groups) |
| [Search Queues](actions/search-queues.md) | `GET queues` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues) |
| [Search Tickets](actions/search-tickets.md) | `GET tickets` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Search Users](actions/search-users.md) | `GET users` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Users) |
| [Steal Ticket](actions/steal-ticket.md) | `PUT ticket/:ticketId/steal` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Take Ticket](actions/take-ticket.md) | `PUT ticket/:ticketId/take` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Untake Ticket](actions/untake-ticket.md) | `PUT ticket/:ticketId/untake` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Update Queue](actions/update-queue.md) | `PUT queue/:queueId` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues) |
| [Update Ticket](actions/update-ticket.md) | `PUT ticket/:ticketId` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets) |
| [Update User](actions/update-user.md) | `PUT user/:userId` | [docs](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Users) |
