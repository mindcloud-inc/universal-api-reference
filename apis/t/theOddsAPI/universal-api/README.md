# <img src="https://images.mindcloud.co/apps/icons/the-odds-api-icon-square_1776180805773.png" alt="The Odds logo" width="28" height="28"> The Odds: Universal API

Official sports odds, scores, events, participants, and historical odds data from The Odds API v4.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/theOddsAPI/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://the-odds-api.com
- **Vendor API docs:** https://the-odds-api.com/liveapi/guides/v4/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sports](actions/list-sports.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-sports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves sports events from The Odds API. |

### Event Market

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Markets](actions/get-event-markets.md) | GET | Retrieves markets for a specific event from The Odds API. |

### Event Odds

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Odds](actions/get-event-odds.md) | GET | Retrieves odds for a specific event from The Odds API. |

### Historical Event Odds Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Event Odds](actions/get-historical-event-odds.md) | GET | Retrieves historical odds for a specific event from The Odds API. |

### Historical Event Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [List Historical Events](actions/list-historical-events.md) | GET | Retrieves historical events from The Odds API. |

### Historical Odds Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [List Historical Odds](actions/list-historical-odds.md) | GET | Retrieves historical odds from The Odds API. |

### Odds Event

| Action | Method | Description |
| --- | --- | --- |
| [List Odds](actions/list-odds.md) | GET | Retrieves odds for sports events from The Odds API. |

### Participant

| Action | Method | Description |
| --- | --- | --- |
| [List Participants](actions/list-participants.md) | GET | Retrieves participants for a sport from The Odds API. |

### Score Event

| Action | Method | Description |
| --- | --- | --- |
| [List Scores](actions/list-scores.md) | GET | Retrieves scores for sports events from The Odds API. |

### Sport

| Action | Method | Description |
| --- | --- | --- |
| [List Sports](actions/list-sports.md) | GET | Retrieves supported sports from The Odds API. |

