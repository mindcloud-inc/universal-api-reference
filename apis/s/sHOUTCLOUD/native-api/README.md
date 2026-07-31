# SHOUTCLOUD: Native API Reference

A consolidated summary of SHOUTCLOUD's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://github.com/SHOUTCLOUD/SHOUTCLOUD_NODE
- **API base URL:** `http://API.SHOUTCLOUD.IO`

## Authentication

### No authentication

The original SHOUTCLOUD transformation endpoint requires no authentication.

This API does not require request authentication.

[Official authentication documentation](https://github.com/SHOUTCLOUD/SHOUTCLOUD_NODE)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Shout Text](actions/shout-text.md) | `POST /V1/SHOUT` | [docs](https://github.com/SHOUTCLOUD/SHOUTCLOUD_NODE/blob/master/SHOUTCLOUD.js) |
