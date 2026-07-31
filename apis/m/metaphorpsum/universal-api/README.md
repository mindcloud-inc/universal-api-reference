# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423657941.png" alt="Metaphorpsum logo" width="28" height="28"> Metaphorpsum: Universal API

Generate Metaphorpsum placeholder paragraphs or sentences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/metaphorpsum/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lorum.casjay.vercel.app/
- **Vendor API docs:** https://lorum.casjay.vercel.app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Metaphor Paragraphs](actions/get-metaphor-paragraphs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaphorpsum/latest/actions/get-metaphor-paragraphs?connectionId=$CONNECTION_ID&paragraphCount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Get Metaphor Paragraphs](actions/get-metaphor-paragraphs.md) | GET |  |
| [Get Metaphor Sentences](actions/get-metaphor-sentences.md) | GET |  |

