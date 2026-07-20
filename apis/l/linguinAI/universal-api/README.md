# <img src="https://images.mindcloud.co/apps/icons/linguin-ai-icon-192_1775497848913.png" alt="Linguin AI logo" width="28" height="28"> Linguin AI: Universal API

Use Linguin AI to detect languages, detect profanity, inspect account usage status, and list supported languages through the official API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linguinAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://linguin.ai/
- **Vendor API docs:** https://linguin.ai/api-docs/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Status](actions/get-account-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Account Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Status](actions/get-account-status.md) | GET |  |

### Bulk Language Detection

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Detect Language](actions/bulk-detect-language.md) | POST |  |

### Bulk Profanity Detection

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Detect Profanity](actions/bulk-detect-profanity.md) | POST |  |

### Language Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect Language](actions/detect-language.md) | POST |  |

### Profanity Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect Profanity](actions/detect-profanity.md) | POST |  |

### Supported Languages

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Languages](actions/list-supported-languages.md) | GET |  |

