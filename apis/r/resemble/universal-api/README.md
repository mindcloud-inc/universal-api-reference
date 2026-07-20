# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-resemble-ai-48x48_1775763194965.png" alt="Resemble logo" width="28" height="28"> Resemble: Universal API

Resemble AI provides APIs for voice generation, speech-to-text, agent orchestration, audio tooling, and voice asset management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/resemble/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.resemble.ai
- **Vendor API docs:** https://docs.resemble.ai/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resemble/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET |  |

