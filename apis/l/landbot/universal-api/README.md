# <img src="https://images.mindcloud.co/apps/icons/landbot_1773417342416.png" alt="Landbot logo" width="28" height="28"> Landbot: Universal API

Manage Landbot channels, customers, and chatbot data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/landbot/latest
- **Category:** Communication / Team Messaging
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://landbot.io/
- **Vendor API docs:** https://api.landbot.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Channel](actions/get-channel.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Landbot. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from Landbot. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Archive Customer](actions/archive-customer.md) | PUT | Archives a customer in Landbot. |
| [Assign Customer](actions/assign-customer.md) | PUT | Assigns a customer in Landbot. |
| [Assign Customer to Agent](actions/assign-customer-to-agent.md) | PUT | Assigns a customer to an agent in Landbot. |
| [Assign Customer to Bot](actions/assign-customer-to-bot.md) | PUT | Assigns a customer to a bot in Landbot. |
| [Block Customer](actions/block-customer.md) | PUT | Blocks a customer in Landbot. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Landbot. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Landbot. |
| [Unarchive Customer](actions/unarchive-customer.md) | PUT | Unarchives a customer in Landbot. |
| [Unassign Customer](actions/unassign-customer.md) | PUT | Unassigns a customer in Landbot. |
| [Unblock Customer](actions/unblock-customer.md) | PUT | Unblocks a customer in Landbot. |

### Customer Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Field](actions/create-customer-field.md) | POST | Creates a customer field in Landbot. |
| [Get Customer Field](actions/get-customer-field.md) | GET | Retrieves a customer field from Landbot. |
| [Update Customer Field](actions/update-customer-field.md) | PUT | Updates a customer field in Landbot. |

### Message Hook

| Action | Method | Description |
| --- | --- | --- |
| [Create Message Hook](actions/create-message-hook.md) | POST | Creates a message hook for a Landbot channel. |
| [Delete Message Hook](actions/delete-message-hook.md) | DELETE | Deletes a message hook from a Landbot channel. |
| [Get Message Hook](actions/get-message-hook.md) | GET | Retrieves a message hook from a Landbot channel. |
| [List Message Hooks](actions/list-message-hooks.md) | GET | Retrieves message hooks for a Landbot channel. |

### Whatsapp Template

| Action | Method | Description |
| --- | --- | --- |
| [List WhatsApp Templates](actions/list-whatsapp-templates.md) | GET | Retrieves WhatsApp templates from Landbot. |

