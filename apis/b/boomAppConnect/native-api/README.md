# boomApp Connect: Native API Reference

A consolidated summary of boomApp Connect's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/boomappconnect/
- **OpenAPI specification:** https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json
- **API base URL:** `https://direct-api.apps.boomcomms.com`

## Authentication

### Basic Authentication

Use the Boomerang API username and password provided for boomApp Connect.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/boomappconnect/#creating-a-connection)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Masked Two-Way SMS Thread](actions/create-masked-two-way-sms-thread.md) | `POST /v1/maskTwoWay` | [docs](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json) |
| [Make Voice Call](actions/make-voice-call.md) | `POST /v1/flat/voice` | [docs](https://learn.microsoft.com/en-us/connectors/boomappconnect/#voice) |
| [Retrieve Delivery Status Updates](actions/retrieve-delivery-status-updates.md) | `GET /v1/get_all_new_drs` | [docs](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json) |
| [Retrieve Inbound Campaign Messages](actions/retrieve-inbound-campaign-messages.md) | `GET /v1/get-inbound` | [docs](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json) |
| [Retrieve Message Responses](actions/retrieve-message-responses.md) | `GET /v1/get_responses` | [docs](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json) |
| [Send Email](actions/send-email.md) | `POST /v1/flat/email` | [docs](https://learn.microsoft.com/en-us/connectors/boomappconnect/#email) |
| [Send SMS From Custom Number](actions/send-sms-from-custom-number.md) | `POST /v1/flat/sms3` | [docs](https://learn.microsoft.com/en-us/connectors/boomappconnect/#sms-custom-number) |
| [Send SMS One-Way](actions/send-sms-one-way.md) | `POST /v1/flat/sms1` | [docs](https://learn.microsoft.com/en-us/connectors/boomappconnect/#sms-one-way) |
| [Send SMS Two-Way](actions/send-sms-two-way.md) | `POST /v1/flat/sms2` | [docs](https://learn.microsoft.com/en-us/connectors/boomappconnect/#sms-two-way) |
