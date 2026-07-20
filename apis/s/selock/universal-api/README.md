# <img src="https://images.mindcloud.co/apps/icons/favicon-selock-co-48x48_1776701025865.png" alt="Selock logo" width="28" height="28"> Selock: Universal API

Selock is a smart-lock and guest self check-in platform for hospitality operations. This app wraps the documented Selock data, order, lock-status, and webhook subscription endpoints using the tenant token contract published in Selock's official docs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/selock/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://selock.co/
- **Vendor API docs:** https://selock.co/en/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Token](actions/verify-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selock/latest/actions/verify-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Battery Alert

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe Battery Alert](actions/subscribe-battery.md) | POST |  |
| [Unsubscribe Battery Alert](actions/unsubscribe-battery.md) | DELETE |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Verify Token](actions/verify-token.md) | GET |  |

### Guest

| Action | Method | Description |
| --- | --- | --- |
| [List Guests](actions/list-guests.md) | GET |  |

### Lock

| Action | Method | Description |
| --- | --- | --- |
| [Change Lock Status](actions/change-lock-status.md) | PUT |  |
| [List Locks](actions/list-locks.md) | GET |  |

### Lock Close Events

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe Lock Close Events](actions/subscribe-locks-close.md) | POST |  |
| [Unsubscribe Lock Close Events](actions/unsubscribe-locks-close.md) | DELETE |  |

### Lock Events

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe Lock Events](actions/subscribe-locks.md) | POST |  |
| [Unsubscribe Lock Events](actions/unsubscribe-locks.md) | DELETE |  |

### Lock Open Events

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe Lock Open Events](actions/subscribe-locks-open.md) | POST |  |
| [Unsubscribe Lock Open Events](actions/unsubscribe-locks-open.md) | DELETE |  |

### New Orders

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe New Orders](actions/subscribe-orders.md) | POST |  |
| [Unsubscribe New Orders](actions/unsubscribe-orders.md) | DELETE |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET |  |

### Order Changes

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe Order Changes](actions/subscribe-orders-change.md) | POST |  |
| [Unsubscribe Order Changes](actions/unsubscribe-orders-change.md) | DELETE |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Change Order](actions/change-order.md) | PUT |  |
| [Create Order](actions/create-order.md) | POST |  |

### Room

| Action | Method | Description |
| --- | --- | --- |
| [List Rooms](actions/list-rooms.md) | GET |  |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET |  |

