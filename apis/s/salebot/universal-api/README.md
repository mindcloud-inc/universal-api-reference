# <img src="https://images.mindcloud.co/apps/icons/salebot_1776781196971.png" alt="Salebot logo" width="28" height="28"> Salebot: Universal API

Manage Salebot CRM clients, variables, deals, callbacks, and messaging workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salebot/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salebot.pro
- **Vendor API docs:** https://docs.salebot.pro/rabota-s-api/api-konstruktora

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [List Connected Channels](actions/list-connected-channels.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Find All Client IDs by Variable](actions/find-all-client-ids-by-variable.md) | GET |  |
| [Find Client ID by Variable](actions/find-client-id-by-variable.md) | GET |  |
| [Find Client IDs by Platform ID](actions/find-client-ids-by-platform-id.md) | GET |  |
| [Find Client IDs by Several Variables](actions/find-client-ids-by-several-variables.md) | GET |  |
| [Find Clients](actions/find-clients.md) | GET |  |
| [Find Latest Client ID by Variable](actions/find-latest-client-id-by-variable.md) | GET |  |
| [Get Variables](actions/get-variables.md) | GET |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Resolve Online Chat Client](actions/resolve-online-chat-client.md) | GET |  |
| [Save Variables](actions/save-variables.md) | PUT |  |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Get Current Order ID](actions/get-current-order-id.md) | GET |  |
| [Get Order State](actions/get-order-state.md) | GET |  |
| [Get Order Variables](actions/get-order-variables.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [Move Order to Next State](actions/move-order-to-next-state.md) | PUT |  |
| [Set Order Variables](actions/set-order-variables.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Clear Message History](actions/clear-message-history.md) | DELETE |  |
| [Get Message History](actions/get-message-history.md) | GET |  |
| [List Bot Messages](actions/list-bot-messages.md) | GET |  |
| [Send Broadcast](actions/send-broadcast.md) | POST |  |
| [Send Callback by Platform ID](actions/send-callback-by-platform-id.md) | POST |  |
| [Send Message](actions/send-message.md) | POST |  |
| [Trigger Callback](actions/trigger-callback.md) | POST |  |
| [Trigger Email Callback](actions/trigger-email-callback.md) | POST |  |

