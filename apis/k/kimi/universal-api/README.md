# <img src="https://images.mindcloud.co/apps/icons/kimi-color_1778178548999.png" alt="Kimi logo" width="28" height="28"> Kimi: Universal API

Use Kimi by Moonshot AI to generate chat completions, estimate tokens, inspect available models and balances, manage files, and run batch API jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kimi/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://platform.kimi.ai
- **Vendor API docs:** https://platform.kimi.ai/docs/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kimi/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | GET | Retrieves your account balance from Kimi. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves your uploaded files from Kimi. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves the available models from Kimi. |

