# <img src="https://images.mindcloud.co/apps/icons/morph_1775252705532.png" alt="Morph logo" width="28" height="28"> Morph: Universal API

Use Morph's coding-agent models and subagents to generate embeddings, edit code, search codebases, and compress context.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/morph/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.morphllm.com/
- **Vendor API docs:** https://docs.morphllm.com/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morph/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Apply Code Changes](actions/apply-code-changes.md) | GET | Applies code changes with Morph. |
| [Compact Context](actions/compact-context.md) | GET | Compacts context with Morph. |
| [Generate Embedding](actions/generate-embedding.md) | GET | Generates embeddings with Morph. |
| [Rerank Documents](actions/rerank-documents.md) | GET | Reranks documents with Morph. |
| [Search Code With WarpGrep](actions/search-code-with-warp-grep.md) | GET | Searches code with Morph WarpGrep. |
| [Verify API Key](actions/verify-api-key.md) | GET | Verifies a Morph API key with a fixed embedding request. |

