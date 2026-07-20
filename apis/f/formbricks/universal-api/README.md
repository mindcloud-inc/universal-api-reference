# <img src="https://images.mindcloud.co/apps/icons/formbricks_1774541733806.png" alt="Formbricks logo" width="28" height="28"> Formbricks: Universal API

Manage Formbricks surveys, responses, contacts, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formbricks/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://formbricks.com
- **Vendor API docs:** https://formbricks.com/docs/api-v2-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Me](actions/get-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Response](actions/create-client-response.md) | POST | Creates a new client response in Formbricks. |
| [Get Response](actions/get-response.md) | GET | Retrieves a response from Formbricks. |
| [Get Responses](actions/get-responses.md) | GET | Retrieves responses from Formbricks. |
| [Update Client Response](actions/update-client-response.md) | PUT | Updates an existing client response in Formbricks. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Me](actions/get-me.md) | GET | Retrieves the current user from Formbricks. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Formbricks. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Formbricks. |
| [Get Webhooks](actions/get-webhooks.md) | GET | Retrieves webhooks from Formbricks. |

