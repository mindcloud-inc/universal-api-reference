# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-13-as-14_1776102066580.png" alt="Straker Verify logo" width="28" height="28"> Straker Verify: Universal API

Verify translations, check quality, and manage human review projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/strakerVerify/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.straker.ai/ai-platform/verify-translate
- **Vendor API docs:** https://api-verify.straker.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Balance](actions/get-token-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strakerVerify/latest/actions/get-token-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Token Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Balance](actions/get-token-balance.md) | GET | Retrieves your token balance from Straker Verify. |

