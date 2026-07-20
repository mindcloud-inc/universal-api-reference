# <img src="https://images.mindcloud.co/apps/icons/89166980_1776459638357.png" alt="Streamer.bot logo" width="28" height="28"> Streamer.bot: Universal API

Connect to Streamer.bot to read credits, inspect actions, and trigger local stream automation over HTTP.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/streamerbot/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://streamer.bot/
- **Vendor API docs:** https://docs.streamer.bot/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Do Action](actions/do-action.md) | POST | Triggers an existing action in Streamer.bot. |
| [Get Actions](actions/get-actions.md) | GET | Retrieves all available actions from Streamer.bot. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Clear Credits](actions/clear-credits.md) | DELETE | Clears the current credits in Streamer.bot. |
| [Get Credits](actions/get-credits.md) | GET | Retrieves the current credits data from Streamer.bot. |
| [Test Credits](actions/test-credits.md) | GET | Tests the current credits data in Streamer.bot. |

### First Word Cache

| Action | Method | Description |
| --- | --- | --- |
| [Clear First Words Cache](actions/clear-first-words-cache.md) | DELETE | Clears the first words cache in Streamer.bot. |

