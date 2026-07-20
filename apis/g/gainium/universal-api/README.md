# <img src="https://images.mindcloud.co/apps/icons/gainium_1777305648269.png" alt="Gainium logo" width="28" height="28"> Gainium: Universal API

Create, run, and analyze crypto trading bots

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gainium/latest
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gainium.io
- **Vendor API docs:** https://api.gainium.io/api/docs/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Exchanges](actions/list-exchanges.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-exchanges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [List Balances](actions/list-balances.md) | GET |  |

### Bot Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Bot Schema Definition](actions/get-bot-schema-definition.md) | GET |  |
| [List Bot Schema Definitions](actions/list-bot-schema-definitions.md) | GET |  |

### Bot Section

| Action | Method | Description |
| --- | --- | --- |
| [List Bot Sections](actions/list-bot-sections.md) | GET |  |

### Combo Backtest Request

| Action | Method | Description |
| --- | --- | --- |
| [List Combo Backtest Requests](actions/list-combo-backtest-requests.md) | GET |  |

### Combo Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Combo Bots](actions/list-combo-bots.md) | GET |  |

### Combo Deal

| Action | Method | Description |
| --- | --- | --- |
| [List Combo Deals](actions/list-combo-deals.md) | GET |  |

### Dca Backtest Request

| Action | Method | Description |
| --- | --- | --- |
| [List DCA Backtest Requests](actions/list-dca-backtest-requests.md) | GET |  |

### Dca Bot

| Action | Method | Description |
| --- | --- | --- |
| [List DCA Bots](actions/list-dca-bots.md) | GET |  |

### Dca Deal

| Action | Method | Description |
| --- | --- | --- |
| [List DCA Deals](actions/list-dca-deals.md) | GET |  |

### Exchange

| Action | Method | Description |
| --- | --- | --- |
| [List Exchanges](actions/list-exchanges.md) | GET |  |

### Global Variable

| Action | Method | Description |
| --- | --- | --- |
| [List Global Variables](actions/list-global-variables.md) | GET |  |

### Grid Backtest Request

| Action | Method | Description |
| --- | --- | --- |
| [List Grid Backtest Requests](actions/list-grid-backtest-requests.md) | GET |  |

### Grid Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Grid Bots](actions/list-grid-bots.md) | GET |  |

### Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get Indicator Definition](actions/get-indicator-definition.md) | GET |  |
| [List Indicator Types](actions/list-indicator-types.md) | GET |  |

### Supported Exchange

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Exchanges](actions/list-supported-exchanges.md) | GET |  |

### Terminal Deal

| Action | Method | Description |
| --- | --- | --- |
| [List Terminal Deals](actions/list-terminal-deals.md) | GET |  |

