# Virtual Summits Software: Native API Reference

A consolidated summary of Virtual Summits Software's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://support.virtualsummits.com/hc/en-us/sections/360013135012-Integrations
- **API base URL:** `https://api.virtualsummits.com/api/v1`

## Authentication

### API Key

Use the Virtual Summits API key from your profile.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.virtualsummits.com/hc/en-us/articles/14314790002580-Zapier-Integration)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Summit](actions/get-summit.md) | `GET /summits/:summitId` | [docs](https://support.virtualsummits.com/hc/en-us/articles/14314790002580-Zapier-Integration) |
| [List Speaker Application Questions](actions/list-speaker-application-questions.md) | `GET /summits/:summitId/speaker-application-questions` |  |
| [List Sponsorship Tiers](actions/list-sponsorship-tiers.md) | `GET /summits/:summitId/sponsorship-tiers` |  |
| [List Summit Attendees](actions/list-summit-attendees.md) | `GET /summits/:summitId/attendees` | [docs](https://support.virtualsummits.com/hc/en-us/articles/14314790002580-Zapier-Integration) |
| [List Summit Categories](actions/list-summit-categories.md) | `GET /summits/:summitId/categories` |  |
| [List Summit Landing Pages](actions/list-summit-landing-pages.md) | `GET /summits/:summitId/landing-pages` |  |
| [List Summit Presentations](actions/list-summit-presentations.md) | `GET /summits/:summitId/presentations` |  |
| [List Summit Sessions](actions/list-summit-sessions.md) | `GET /summits/:summitId/summit-sessions` |  |
| [List Summit Sponsors](actions/list-summit-sponsors.md) | `GET /summits/:summitId/sponsors` |  |
| [List Summits](actions/list-summits.md) | `GET /summits` | [docs](https://support.virtualsummits.com/hc/en-us/articles/14314790002580-Zapier-Integration) |
| [List Tier Items](actions/list-tier-items.md) | `GET /summits/:summitId/tier-items` |  |
| [List Tier Levels](actions/list-tier-levels.md) | `GET /summits/:summitId/tier-levels` |  |
