# Charidy: Native API Reference

A consolidated summary of Charidy's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/1118680/S1a4WS4g
- **API base URL:** `https://api.charidy.com`

## Authentication

### No Authentication

Charidy public API endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://articles.charidy.com/hc/en-us/articles/4561905476116-Access-Charidy-s-Public-API)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | `GET /api/v1/campaign/:campaignId` | [docs](https://documenter.getpostman.com/view/1118680/S1a4WS4g) |
| [List Campaign Donations](actions/list-campaign-donations.md) | `GET /api/v1/campaign/:campaignId/donations` | [docs](https://documenter.getpostman.com/view/1118680/S1a4WS4g) |
| [List Campaign Teams](actions/list-campaign-teams.md) | `GET /api/v1/campaign/:campaignId/teams` | [docs](https://documenter.getpostman.com/view/1118680/S1a4WS4g) |
