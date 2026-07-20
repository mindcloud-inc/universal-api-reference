# ProxiedMail: Native API Reference

A consolidated summary of ProxiedMail's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.proxiedmail.com/docs/intro/
- **API base URL:** `https://proxiedmail.com/api/v1`

## Authentication

### API Key

Connect with a ProxiedMail API token from Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Token: <apiKey>
```

[Official authentication documentation](https://docs.proxiedmail.com/docs/endpoints/tokensDifference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate With Username And Password](actions/authenticate-with-username-and-password.md) | `POST /auth` | [docs](https://docs.proxiedmail.com/docs/endpoints/login/) |
| [Create Built-In Webhook Receiver](actions/create-built-in-webhook-receiver.md) | `POST /callback` | [docs](https://docs.proxiedmail.com/docs/webhookscr/create/) |
| [Create Proxy Binding](actions/create-proxy-binding.md) | `POST /proxy-bindings` | [docs](https://docs.proxiedmail.com/docs/endpoints/postproxybindings/) |
| [Exchange Bearer Token For API Token](actions/exchange-bearer-token-for-api-token.md) | `GET /api-token` | [docs](https://docs.proxiedmail.com/docs/endpoints/apitoken/) |
| [Get Built-In Webhook Receiver Payload](actions/get-built-in-webhook-receiver-payload.md) | `GET /callback/get/:hash` | [docs](https://docs.proxiedmail.com/docs/webhookscr/get/) |
| [Get Received Email Details](actions/get-received-email-details.md) | `GET /received-emails/:receivedEmailId` | [docs](https://docs.proxiedmail.com/docs/endpoints/getreceivedemails/) |
| [Inspect Proxy Binding Quota Usage](actions/inspect-proxy-binding-quota-usage.md) | `GET /proxy-bindings` | [docs](https://docs.proxiedmail.com/docs/endpoints/getproxybindings/) |
| [List Proxy Bindings](actions/list-proxy-bindings.md) | `GET /proxy-bindings` | [docs](https://docs.proxiedmail.com/docs/endpoints/getproxybindings/) |
| [List Received Email Links](actions/list-received-email-links.md) | `GET /received-emails-links/:proxyBindingId` | [docs](https://docs.proxiedmail.com/docs/endpoints/receivedemailslinks/) |
| [Update Proxy Binding](actions/update-proxy-binding.md) | `PATCH /proxy-bindings/:proxyBindingId` | [docs](https://docs.proxiedmail.com/docs/endpoints/patchproxybindings/) |
