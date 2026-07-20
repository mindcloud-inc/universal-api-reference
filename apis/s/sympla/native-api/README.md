# Sympla: Native API Reference

A consolidated summary of Sympla's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developers.sympla.com.br/api-doc/index.html
- **API base URL:** `https://api.sympla.com.br/public/v1.5.1`

## Authentication

### API Key

Create a public API token in the Sympla organizer account under Minha Conta > Integracoes and paste it here as the API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ajuda.produtor.sympla.com.br/hc/pt-br/articles/15422073696653-Como-configurar-API-publica)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `field_sort` in the query string. Set the direction separately with `sort`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check In Participant](actions/check-in-participant.md) | `POST /events/:eventId/participants/:participantId/checkin` | [docs](https://developers.sympla.com.br/api-doc/index.html#operation/checkInByParticipantId) |
| [Get Event By ID](actions/get-event-by-id.md) | `GET /events/:eventId` | [docs](https://developers.sympla.com.br/api-doc/index.html#operation/getEventId) |
| [Get Order By ID](actions/get-order-by-id.md) | `GET /events/:eventId/orders/:orderId` | [docs](https://developers.sympla.com.br/api-doc/index.html#operation/getOneOrder) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developers.sympla.com.br/api-doc/index.html#operation/getAllEvent) |
| [List Orders By Event](actions/list-orders-by-event.md) | `GET /events/:eventId/orders` | [docs](https://developers.sympla.com.br/api-doc/index.html#operation/getListOrders) |
| [List Participants By Event](actions/list-participants-by-event.md) | `GET /events/:eventId/participants` | [docs](https://developers.sympla.com.br/api-doc/index.html#operation/getAllParticipants) |
| [List Participants By Order](actions/list-participants-by-order.md) | `GET /events/:eventId/orders/:orderId/participants` | [docs](https://developers.sympla.com.br/api-doc/index.html#operation/getAllParticipantsForOrder) |
