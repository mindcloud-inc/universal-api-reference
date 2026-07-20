# <img src="https://images.mindcloud.co/apps/icons/notify_1775682219785.png" alt="Notify logo" width="28" height="28"> Notify: Universal API

Send web push notifications to Notify channels, inspect channel metadata and recent delivery results, and manage browser subscription payloads against notify.run.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/notify/latest
- **Category:** Communication / Team Messaging
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://notify.run
- **Vendor API docs:** https://notify.run

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Channel Info](actions/get-current-channel-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notify/latest/actions/get-current-channel-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Public Key](actions/get-channel-public-key.md) | GET | Retrieves the channel public key from Notify. |
| [Get Current Channel Public Key](actions/get-current-channel-public-key.md) | GET | Retrieves the current channel public key from Notify. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Notify. |
| [Get Channel Info](actions/get-channel-info.md) | GET | Retrieves channel details from Notify. |
| [Get Current Channel Info](actions/get-current-channel-info.md) | GET | Retrieves current channel details from Notify. |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Endpoint URL](actions/get-channel-endpoint-url.md) | GET | Retrieves the channel endpoint URL from Notify. |
| [Get Channel Page URL](actions/get-channel-page-url.md) | GET | Retrieves the channel page URL from Notify. |
| [Get Channel URLs](actions/get-channel-ur-ls.md) | GET | Retrieves channel URLs from Notify. |
| [Get Current Channel Endpoint URL](actions/get-current-channel-endpoint-url.md) | GET | Retrieves the current channel endpoint URL from Notify. |
| [Get Current Channel Page URL](actions/get-current-channel-page-url.md) | GET | Retrieves the current channel page URL from Notify. |
| [Get Current Channel URLs](actions/get-current-channel-ur-ls.md) | GET | Retrieves current channel URLs from Notify. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel QR Code](actions/get-channel-qr-code.md) | GET | Retrieves the channel QR code from Notify. |
| [Get Current Channel QR Code](actions/get-current-channel-qr-code.md) | GET | Retrieves the current channel QR code from Notify. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Channel Message](actions/get-latest-channel-message.md) | GET | Retrieves the latest channel message from Notify. |
| [Get Latest Current Channel Message](actions/get-latest-current-channel-message.md) | GET | Retrieves the latest current channel message from Notify. |
| [List Channel Messages](actions/list-channel-messages.md) | GET | Retrieves channel messages from Notify. |
| [List Current Channel Messages](actions/list-current-channel-messages.md) | GET | Retrieves current channel messages from Notify. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Delivery Results](actions/list-channel-delivery-results.md) | GET | Retrieves channel delivery results from Notify. |
| [List Current Channel Delivery Results](actions/list-current-channel-delivery-results.md) | GET | Retrieves current channel delivery results from Notify. |
| [Send Channel Message](actions/send-channel-message.md) | POST | Creates a new message in a Notify channel. |
| [Send Current Channel Message](actions/send-current-channel-message.md) | POST | Creates a new message in the current Notify channel. |

