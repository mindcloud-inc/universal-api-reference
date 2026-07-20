# Zoom Scheduler: Native API Reference

A consolidated summary of Zoom Scheduler's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developers.zoom.us/docs/api/scheduler/
- **OpenAPI specification:** https://developers.zoom.us/api-hub/scheduler/methods/endpoints.json
- **API base URL:** `https://api.zoom.us/v2`

## Authentication

### Zoom OAuth2

OAuth2 authorization for Zoom Scheduler API access

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://zoom.us/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://zoom.us/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `scheduler:delete:availability scheduler:delete:availability:admin scheduler:delete:delete_schedule scheduler:delete:delete_schedule:admin scheduler:delete:scheduled_event scheduler:delete:scheduled_event:admin scheduler:read:analytics scheduler:read:analytics:admin scheduler:read:availability scheduler:read:availability:admin scheduler:read:get_schedule scheduler:read:get_schedule:admin scheduler:read:list_availability scheduler:read:list_availability:admin scheduler:read:list_schedule scheduler:read:list_schedule:admin scheduler:read:list_scheduled_events scheduler:read:list_scheduled_events:admin scheduler:read:routing scheduler:read:routing:admin scheduler:read:scheduled_event scheduler:read:scheduled_event:admin scheduler:read:scheduled_event_attendee scheduler:read:scheduled_event_attendee:admin scheduler:read:user scheduler:read:user:admin scheduler:update:availability scheduler:update:availability:admin scheduler:update:patch_schedule scheduler:update:patch_schedule:admin scheduler:update:scheduled_event scheduler:update:scheduled_event:admin scheduler:write:availability scheduler:write:availability:admin scheduler:write:insert_schedule scheduler:write:insert_schedule:admin scheduler:write:share scheduler:write:share:admin scheduler:write:single_use_link scheduler:write:single_use_link:admin`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://zoom.us/oauth/token.

[Official authentication documentation](https://developers.zoom.us/docs/integrations/oauth/)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | `GET scheduler/teams` | [docs](https://developers.zoom.us/docs/api/scheduler/) |
