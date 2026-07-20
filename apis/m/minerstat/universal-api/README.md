# <img src="https://images.mindcloud.co/apps/icons/minerstat_1776279366030.png" alt="Minerstat logo" width="28" height="28"> Minerstat: Universal API

Track mining coin, hardware, and pool data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/minerstat/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://minerstat.com
- **Vendor API docs:** https://api.minerstat.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Coins](actions/list-coins.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-coins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Coin

| Action | Method | Description |
| --- | --- | --- |
| [List Coins](actions/list-coins.md) | GET | Retrieves coins from the Minerstat catalog. |

### Hardware

| Action | Method | Description |
| --- | --- | --- |
| [List Hardware](actions/list-hardware.md) | GET | Retrieves mining hardware from the Minerstat catalog. |

### Pool

| Action | Method | Description |
| --- | --- | --- |
| [List Pools](actions/list-pools.md) | GET | Retrieves mining pools from the Minerstat catalog. |

