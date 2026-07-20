# <img src="https://images.mindcloud.co/apps/icons/images-19_1776186964077.png" alt="Vectorizer AI logo" width="28" height="28"> Vectorizer AI: Universal API

Bitmap vectorization API for tracing images into SVG and other vector formats.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vectorizerAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vectorizer.ai/
- **Vendor API docs:** https://vectorizer.ai/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Account Status](actions/account-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Account Status](actions/account-status.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete](actions/delete.md) | DELETE |  |
| [Download](actions/download.md) | GET |  |
| [Vectorize](actions/vectorize.md) | POST |  |

