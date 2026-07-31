# <img src="https://images.mindcloud.co/apps/icons/urban-dictionary_1785426415085.png" alt="Urban Dictionary logo" width="28" height="28"> Urban Dictionary: Universal API

Look up community-submitted slang definitions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/urbanDictionary/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.urbandictionary.com
- **Vendor API docs:** https://api.urbandictionary.com/v0/define

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Look Up Definitions](actions/look-up-definitions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urbanDictionary/latest/actions/look-up-definitions?connectionId=$CONNECTION_ID&term=e.g.%2C%20yeet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Definition Results

| Action | Method | Description |
| --- | --- | --- |
| [Look Up Definitions](actions/look-up-definitions.md) | GET |  |

