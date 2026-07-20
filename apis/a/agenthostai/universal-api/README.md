# <img src="https://images.mindcloud.co/apps/icons/agenthostai_1775146963872.png" alt="Agenthost.ai logo" width="28" height="28"> Agenthost.ai: Universal API

Build and launch AI chatbots, tools, and connected apps

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agenthostai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.agenthost.ai
- **Vendor API docs:** https://docs.agenthost.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Message Limit](actions/get-user-message-limit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/get-user-message-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Subscription Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Available Plans](actions/list-available-plans.md) | GET | Retrieves available subscription plans from Agenthost.ai. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Log In](actions/log-in.md) | POST | Starts or completes Agenthost.ai login by email verification. |

### User Message Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get User Message Limit](actions/get-user-message-limit.md) | GET | Retrieves a user's message limit from Agenthost.ai. |

