# <img src="https://images.mindcloud.co/apps/icons/shopia-favicon-4_1775240669476.png" alt="Shopia logo" width="28" height="28"> Shopia: Universal API

Build and run AI content automations for blog and marketing workflows with Shopia.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shopia/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.axelerate.ai/
- **Vendor API docs:** https://docs.axelerate.ai/en/collections/8820825-integrations-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Article Ideas](actions/generate-article-ideas.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopia/latest/actions/generate-article-ideas" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topic": "Productivity workflows",
  "audience": "SaaS founders"
}'
```

## Actions (1)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Generate Article Ideas](actions/generate-article-ideas.md) | POST |  |

