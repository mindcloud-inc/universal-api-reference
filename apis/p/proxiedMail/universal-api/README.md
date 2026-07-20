# <img src="https://images.mindcloud.co/apps/icons/proxied-mail_1774902055288.png" alt="ProxiedMail logo" width="28" height="28"> ProxiedMail: Universal API

Create proxy emails and receive email webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proxiedMail/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://proxiedmail.com
- **Vendor API docs:** https://docs.proxiedmail.com/docs/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Proxy Bindings](actions/list-proxy-bindings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-proxy-bindings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Exchange Bearer Token For API Token](actions/exchange-bearer-token-for-api-token.md) | GET |  |

### Bearer Token

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate With Username And Password](actions/authenticate-with-username-and-password.md) | POST |  |

### Proxy Binding

| Action | Method | Description |
| --- | --- | --- |
| [Create Proxy Binding](actions/create-proxy-binding.md) | POST |  |
| [List Proxy Bindings](actions/list-proxy-bindings.md) | GET |  |
| [Update Proxy Binding](actions/update-proxy-binding.md) | PUT |  |

### Proxy Binding Quota

| Action | Method | Description |
| --- | --- | --- |
| [Inspect Proxy Binding Quota Usage](actions/inspect-proxy-binding-quota-usage.md) | GET |  |

### Received Email Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Received Email Details](actions/get-received-email-details.md) | GET |  |

### Received Email Link

| Action | Method | Description |
| --- | --- | --- |
| [List Received Email Links](actions/list-received-email-links.md) | GET |  |

### Webhook Receiver

| Action | Method | Description |
| --- | --- | --- |
| [Create Built-In Webhook Receiver](actions/create-built-in-webhook-receiver.md) | POST |  |

### Webhook Receiver Payload

| Action | Method | Description |
| --- | --- | --- |
| [Get Built-In Webhook Receiver Payload](actions/get-built-in-webhook-receiver-payload.md) | GET |  |

