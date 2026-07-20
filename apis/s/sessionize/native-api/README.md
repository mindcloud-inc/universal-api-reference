# Sessionize: Native API Reference

A consolidated summary of Sessionize's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://sessionize.com/playbook/api
- **API base URL:** `https://sessionize.com`

## Authentication

### No authentication

Sessionize public JSON API endpoints are read-only and do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://sessionize.com/playbook/api)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Event Data](actions/get-all-event-data.md) | `GET /api/v2/:endpointId/view/All` | [docs](https://sessionize.com/playbook/api) |
| [List Schedule Days](actions/list-schedule-days.md) | `GET /api/v2/:endpointId/view/GridSmart` | [docs](https://sessionize.com/playbook/api) |
| [List Session Groups](actions/list-session-groups.md) | `GET /api/v2/:endpointId/view/Sessions` | [docs](https://sessionize.com/playbook/api) |
| [List Speaker Wall](actions/list-speaker-wall.md) | `GET /api/v2/:endpointId/view/SpeakerWall` | [docs](https://sessionize.com/playbook/api) |
| [List Speakers](actions/list-speakers.md) | `GET /api/v2/:endpointId/view/Speakers` | [docs](https://sessionize.com/playbook/api) |
