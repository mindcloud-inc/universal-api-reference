# <img src="https://images.mindcloud.co/apps/icons/basalt_1782741419577.png" alt="Basalt logo" width="28" height="28"> Basalt: Universal API

Manage prompts, datasets, experiments, and AI observability

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/basalt/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getbasalt.ai
- **Vendor API docs:** https://docs.getbasalt.ai/v1/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Prompts](actions/list-prompts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basalt/latest/actions/list-prompts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves a list of prompts from Basalt. |

