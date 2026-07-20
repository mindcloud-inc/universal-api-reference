# <img src="https://images.mindcloud.co/apps/icons/g-ptbots_1776088941775.png" alt="GPTBots logo" width="28" height="28"> GPTBots: Universal API

GPTBots is an enterprise AI agent platform with REST APIs for conversations, workflows, knowledge bases, databases, users, analytics, and account data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gPTBots/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gptbots.ai
- **Vendor API docs:** https://www.gptbots.ai/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Agent Information](actions/get-agent-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTBots/latest/actions/get-agent-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Information](actions/get-agent-information.md) | GET | Retrieves the configured agent information from GPTBots. |

