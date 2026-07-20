# <img src="https://images.mindcloud.co/apps/icons/unnamed_1775679402558.png" alt="GoZen DeepAgent logo" width="28" height="28"> GoZen DeepAgent: Universal API

Automate customer chats, capture leads, and manage chatbot workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goZenDeepAgent/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gozen.io/deepagent
- **Vendor API docs:** https://docs.gozen.io/deepagent/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your GoZen DeepAgent user profile. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Register Webhook](actions/register-webhook.md) | POST | Registers a webhook in GoZen DeepAgent. |
| [Unregister Webhook](actions/unregister-webhook.md) | DELETE | Unregisters a webhook in GoZen DeepAgent. |

