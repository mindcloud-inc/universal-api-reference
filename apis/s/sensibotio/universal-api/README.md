# <img src="https://images.mindcloud.co/apps/icons/sensibot-1_1777386506480.png" alt="Sensibot.io logo" width="28" height="28"> Sensibot.io: Universal API

AI-powered WhatsApp automation platform for customer engagement and support.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sensibotio/latest
- **Category:** Support / Contact Center
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sensibot.io/
- **Vendor API docs:** https://api.sensibot.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Assistant](actions/get-assistant.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/get-assistant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Assistant Bot Type](actions/assistant-bot-type.md) | PUT | Updates the assistant bot type in Sensibot.io. |
| [Assistant Welcome Message](actions/assistant-welcome-message.md) | PUT | Updates the assistant welcome message in Sensibot.io. |
| [Get Assistant](actions/get-assistant.md) | GET | Retrieves assistant details from Sensibot.io. |
| [Human Takeover](actions/human-takeover.md) | PUT | Updates human takeover mode in Sensibot.io. |
| [WhatsApp Bot Status](actions/whats-app-bot-status.md) | PUT | Updates the WhatsApp beta bot status in Sensibot.io. |
| [WhatsApp Cloud Bot Status](actions/whats-app-cloud-bot-status.md) | PUT | Updates the WhatsApp Cloud bot status in Sensibot.io. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [All Chat History](actions/all-chat-history.md) | GET | Retrieves filtered chat history from Sensibot.io. |
| [Chat History](actions/chat-history.md) | GET | Retrieves chat history for a recipient from Sensibot.io. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer List](actions/create-customer-list.md) | POST | Creates a new customer list in Sensibot.io. |
| [Customer List](actions/customer-list.md) | GET | Retrieves customer lists from Sensibot.io. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp beta Send Chat](actions/whats-app-beta-send-chat.md) | POST | Sends a WhatsApp beta chat message through Sensibot.io. |
| [WhatsApp beta Send Chat [GET]](actions/whats-app-beta-send-chat-get.md) | POST | Sends a WhatsApp beta chat message through Sensibot.io using GET. |
| [WhatsApp Cloud Send Message](actions/whats-app-cloud-send-message.md) | POST | Sends a WhatsApp Cloud message through Sensibot.io. |
| [WhatsApp Cloud Template Send Message](actions/whats-app-cloud-template-send-message.md) | POST | Sends a WhatsApp Cloud template message through Sensibot.io. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Subscriber Info](actions/subscriber-info.md) | GET | Retrieves subscriber details from Sensibot.io. |
| [Subscriber Variables](actions/subscriber-variables.md) | GET | Retrieves subscriber variables from Sensibot.io. |

