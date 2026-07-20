# <img src="https://images.mindcloud.co/apps/icons/vercel-aigateway-chat-model_1775828060806.png" alt="Vercel AI Gateway Chat Model logo" width="28" height="28"> Vercel AI Gateway Chat Model: Universal API

Generate, embed, and inspect AI Gateway model activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vercelAIGatewayChatModel/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vercel.com/ai-gateway
- **Vendor API docs:** https://vercel.com/docs/ai-gateway

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves AI Gateway credit balance and spend from Vercel. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | GET | Retrieves a specific model from Vercel AI Gateway. |
| [Get Model Endpoints](actions/get-model-endpoints.md) | GET | Retrieves provider endpoints for a specific Vercel AI Gateway model. |
| [List Models](actions/list-models.md) | GET | Retrieves available models from Vercel AI Gateway. |

