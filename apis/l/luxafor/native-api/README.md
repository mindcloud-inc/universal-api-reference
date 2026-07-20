# Luxafor: Native API Reference

A consolidated summary of Luxafor's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines
- **API base URL:** `https://api.luxafor.com/webhook/v1/actions`

## Authentication

### Luxafor ID

Use your Luxafor ID from the Webhook tab in Luxafor software.

### Credentials

- **Luxafor ID:** `userId` · required · Find this on the Webhook tab in Luxafor software.

This API does not require request authentication.

[Official authentication documentation](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Blink Device](actions/blink-device.md) | `POST /blink` | [docs](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines) |
| [Play Pattern](actions/play-pattern.md) | `POST /pattern` | [docs](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines) |
| [Set Solid Base Color](actions/set-solid-base-color.md) | `POST /solid_color` | [docs](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines) |
| [Set Solid Custom Color](actions/set-solid-custom-color.md) | `POST /solid_color` | [docs](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines) |
