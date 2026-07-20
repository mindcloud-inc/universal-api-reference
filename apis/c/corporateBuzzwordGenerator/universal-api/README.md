# <img src="https://images.mindcloud.co/apps/icons/corporate-buzzword-generator_1777488278409.png" alt="Corporate Buzzword Generator logo" width="28" height="28"> Corporate Buzzword Generator: Universal API

Generate random corporate buzzwords and jargon

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/corporateBuzzwordGenerator/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://corporatebs-generator.sameerkumar.website
- **Vendor API docs:** https://github.com/sameerkumar18/corporate-bs-generator-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Corporate Buzzword](actions/generate-corporate-buzzword.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corporateBuzzwordGenerator/latest/actions/generate-corporate-buzzword?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Corporate Buzzword

| Action | Method | Description |
| --- | --- | --- |
| [Generate Corporate Buzzword](actions/generate-corporate-buzzword.md) | GET | Retrieves a random corporate buzzword phrase from Corporate Buzzword Generator. |

