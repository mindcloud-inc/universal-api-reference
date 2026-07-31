# <img src="https://images.mindcloud.co/apps/icons/techy_1785427032757.png" alt="Techy logo" width="28" height="28"> Techy: Universal API

Generate random tech-savvy phrases from the public Techy API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/techy/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://techy-api.vercel.app/
- **Vendor API docs:** https://github.com/PerryPal21/Techy-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Techy Phrase](actions/get-random-techy-phrase.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/techy/latest/actions/get-random-techy-phrase?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Techy Phrase

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Techy Phrase](actions/get-random-techy-phrase.md) | GET |  |
| [Get Random Techy Phrase Text](actions/get-random-techy-phrase-text.md) | GET |  |

