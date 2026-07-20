# GoSquared: Native API Reference

A consolidated summary of GoSquared's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://www.gosquared.com/docs/
- **API base URL:** `https://api.gosquared.com`

## Authentication

### API Key

Use a GoSquared API key and, for most endpoints, a site token.

### Credentials

- **API Key:** `apiKey` · required
- **Site Token:** `siteToken` · optional · The token for the GoSquared project you want to query.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.gosquared.com/docs/configuration/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; maximum 250). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contain`.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Blocked Bots Setting](actions/get-blocked-bots-setting.md) | `GET account/v1/blocked/bots` | [docs](https://www.gosquared.com/docs/account/blocked/) |
| [Get Person](actions/get-person.md) | `GET people/v1/people/:personID` | [docs](https://www.gosquared.com/docs/people/people/) |
| [Get Person Feed](actions/get-person-feed.md) | `GET people/v1/people/:personID/feed` | [docs](https://www.gosquared.com/docs/people/people/) |
| [Get Smart Group](actions/get-smart-group.md) | `GET people/v1/smartgroups/:groupID` | [docs](https://www.gosquared.com/docs/people/smartgroups/) |
| [List Active Chats](actions/list-active-chats.md) | `GET chat/v1/chats` | [docs](https://www.gosquared.com/docs/chat/chats/) |
| [List Archived Chats](actions/list-archived-chats.md) | `GET chat/v1/archivedChats` | [docs](https://www.gosquared.com/docs/chat/archivedChats/) |
| [List Blocked IPs](actions/list-blocked-ips.md) | `GET account/v1/blocked/ips` | [docs](https://www.gosquared.com/docs/account/blocked/) |
| [List Blocked Visitors](actions/list-blocked-visitors.md) | `GET account/v1/blocked/visitors` | [docs](https://www.gosquared.com/docs/account/blocked/) |
| [List Devices](actions/list-devices.md) | `GET people/v1/devices` | [docs](https://www.gosquared.com/docs/people/devices/) |
| [List Event Types](actions/list-event-types.md) | `GET people/v1/eventTypes` | [docs](https://www.gosquared.com/docs/people/eventTypes/) |
| [List Property Types](actions/list-property-types.md) | `GET people/v1/propertyTypes` | [docs](https://www.gosquared.com/docs/people/propertyTypes/) |
| [List Shared Users](actions/list-shared-users.md) | `GET account/v1/sharedUsers` | [docs](https://www.gosquared.com/docs/account/sharedUsers/) |
| [List Sites](actions/list-sites.md) | `GET account/v1/sites` | [docs](https://www.gosquared.com/docs/account/sites/) |
| [List Smart Group People](actions/list-smart-group-people.md) | `GET people/v1/smartgroups/:groupID/people` | [docs](https://www.gosquared.com/docs/people/smartgroups/) |
| [List Smart Groups](actions/list-smart-groups.md) | `GET people/v1/smartgroups` | [docs](https://www.gosquared.com/docs/people/smartgroups/) |
| [List Tagged Visitors](actions/list-tagged-visitors.md) | `GET account/v1/taggedVisitors` | [docs](https://www.gosquared.com/docs/account/taggedVisitors/) |
| [List Trigger Types](actions/list-trigger-types.md) | `GET account/v1/triggerTypes` | [docs](https://www.gosquared.com/docs/account/triggerTypes/) |
| [List Webhooks](actions/list-webhooks.md) | `GET account/v1/webhooks` | [docs](https://www.gosquared.com/docs/account/webhooks/) |
| [Search People](actions/search-people.md) | `GET people/v1/people` | [docs](https://www.gosquared.com/docs/people/people/) |
