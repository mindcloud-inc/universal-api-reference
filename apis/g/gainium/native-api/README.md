# Gainium: Native API Reference

A consolidated summary of Gainium's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://api.gainium.io/api/docs/v2
- **OpenAPI specification:** https://api.gainium.io/api/v2/openapi.yaml?view=true
- **API base URL:** `https://api.gainium.io`

## Authentication

### Provider-native Gainium API key

Connect Gainium with an API key and API secret.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · Used to sign Gainium API requests with HMAC-SHA256.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://gainium.io/help/gainium-api-for-developers)

## API conventions

Response data is read from `data`. The current page number is read from `meta.page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Bot Schema Definition](actions/get-bot-schema-definition.md) | `GET /api/v2/discovery/bots/:botType` | [docs](https://api.gainium.io/api/docs/v2#/Discovery/getDiscoveryBot) |
| [Get Indicator Definition](actions/get-indicator-definition.md) | `GET /api/v2/discovery/indicators/:type` | [docs](https://api.gainium.io/api/docs/v2#/Discovery/getDiscoveryIndicator) |
| [List Balances](actions/list-balances.md) | `GET /api/v2/user/balances` | [docs](https://api.gainium.io/api/docs/v2#/User/getUserBalances) |
| [List Bot Schema Definitions](actions/list-bot-schema-definitions.md) | `GET /api/v2/discovery/bots` | [docs](https://api.gainium.io/api/docs/v2#/Discovery/getDiscoveryBots) |
| [List Bot Sections](actions/list-bot-sections.md) | `GET /api/v2/discovery/bots/:botType/sections` | [docs](https://api.gainium.io/api/docs/v2#/Discovery/getDiscoveryBotSections) |
| [List Combo Backtest Requests](actions/list-combo-backtest-requests.md) | `GET /api/v2/backtest/combo/requests` | [docs](https://api.gainium.io/api/docs/v2#/Backtest/getComboBacktestRequests) |
| [List Combo Bots](actions/list-combo-bots.md) | `GET /api/v2/bots/combo` | [docs](https://api.gainium.io/api/docs/v2#/Bots%20-%20Combo/getComboBots) |
| [List Combo Deals](actions/list-combo-deals.md) | `GET /api/v2/deals/combo` | [docs](https://api.gainium.io/api/docs/v2#/Deals%20-%20Combo/getComboDeals) |
| [List DCA Backtest Requests](actions/list-dca-backtest-requests.md) | `GET /api/v2/backtest/dca/requests` | [docs](https://api.gainium.io/api/docs/v2#/Backtest/getDcaBacktestRequests) |
| [List DCA Bots](actions/list-dca-bots.md) | `GET /api/v2/bots/dca` | [docs](https://api.gainium.io/api/docs/v2#/Bots%20-%20DCA/getDCABots) |
| [List DCA Deals](actions/list-dca-deals.md) | `GET /api/v2/deals/dca` | [docs](https://api.gainium.io/api/docs/v2#/Deals%20-%20DCA/getDCADeals) |
| [List Exchanges](actions/list-exchanges.md) | `GET /api/v2/user/exchanges` | [docs](https://api.gainium.io/api/docs/v2#/User/getUserExchanges) |
| [List Global Variables](actions/list-global-variables.md) | `GET /api/v2/user/global-vars` | [docs](https://api.gainium.io/api/docs/v2#/User/getUserGlobalVariables) |
| [List Grid Backtest Requests](actions/list-grid-backtest-requests.md) | `GET /api/v2/backtest/grid/requests` | [docs](https://api.gainium.io/api/docs/v2#/Backtest/getGridBacktestRequests) |
| [List Grid Bots](actions/list-grid-bots.md) | `GET /api/v2/bots/grid` | [docs](https://api.gainium.io/api/docs/v2#/Bots%20-%20Grid/getGridBots) |
| [List Indicator Types](actions/list-indicator-types.md) | `GET /api/v2/discovery/indicators` | [docs](https://api.gainium.io/api/docs/v2#/Discovery/getDiscoveryIndicators) |
| [List Supported Exchanges](actions/list-supported-exchanges.md) | `GET /api/v2/exchanges` | [docs](https://api.gainium.io/api/docs/v2#/General/getUserExchanges) |
| [List Terminal Deals](actions/list-terminal-deals.md) | `GET /api/v2/deals/terminal` | [docs](https://api.gainium.io/api/docs/v2#/Terminal/getTerminalDeals) |
