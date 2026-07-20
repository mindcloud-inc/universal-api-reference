# Lead2Team: Native API Reference

A consolidated summary of Lead2Team's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://wiki.lead2team.com/docs-category/add-the-widget-to-your-website/
- **API base URL:** `https://public-api.lead2team.com/v1`

## Authentication

### API Key

Private API key generated in Lead2Team Web Widget settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://wiki.lead2team.com/docs/wordpress-official-plugin-add-the-widget-to-your-website/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Widget ID](actions/get-widget-id.md) | `POST /getWidgetID` | [docs](https://wiki.lead2team.com/docs/wordpress-official-plugin-add-the-widget-to-your-website/) |
| [List Locations](actions/list-locations.md) | `POST /getLocations` | [docs](https://wiki.lead2team.com/docs/wordpress-official-plugin-add-the-widget-to-your-website/) |
| [List Profiles](actions/list-profiles.md) | `POST /getProfiles` | [docs](https://wiki.lead2team.com/docs/wordpress-official-plugin-add-the-widget-to-your-website/) |
| [List Teams](actions/list-teams.md) | `POST /getTeams` | [docs](https://wiki.lead2team.com/docs/wordpress-official-plugin-add-the-widget-to-your-website/) |
