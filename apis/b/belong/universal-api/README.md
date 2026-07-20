# <img src="https://images.mindcloud.co/apps/icons/belongnet_1775573831695.jpeg" alt="Belong logo" width="28" height="28"> Belong: Universal API

Belong is a token-gated events, memberships, and venue engagement platform with APIs for events, hubs, notes, addresses, QR pass workflows, and on-chain collection flows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/belong/latest
- **Category:** Support / Ticketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://belong.net
- **Vendor API docs:** https://api.belong.net/api/v3/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Profile](actions/get-current-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Search Address Suggestions](actions/search-address-suggestions.md) | GET | Finds address suggestions in Belong by search text. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Belong by ID or slug. |
| [List Events](actions/list-events.md) | GET | Retrieves all available events from Belong. |
| [Search Nearby Events](actions/search-nearby-events.md) | GET | Finds nearby events in Belong by coordinates. |

### Hub

| Action | Method | Description |
| --- | --- | --- |
| [Get Hub](actions/get-hub.md) | GET | Retrieves a hub from Belong by ID or slug. |
| [List Hubs](actions/list-hubs.md) | GET | Retrieves all available hubs from Belong. |
| [List Related Hubs](actions/list-related-hubs.md) | GET | Retrieves related hubs from Belong by hub ID or slug. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Note](actions/get-note.md) | GET | Retrieves a note from Belong by ID. |
| [List Notes](actions/list-notes.md) | GET | Retrieves all note entries from Belong. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Profile](actions/get-current-user-profile.md) | GET | Retrieves the current user profile from Belong. |

