# <img src="https://images.mindcloud.co/apps/icons/meow-facts_1785360823362.png" alt="Meow Facts logo" width="28" height="28"> Meow Facts: Universal API

Get randomized and localized cat facts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/meowFacts/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com/wh-iterabb-it/meowfacts
- **Vendor API docs:** https://github.com/wh-iterabb-it/meowfacts

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get cat facts](actions/get-cat-facts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meowFacts/latest/actions/get-cat-facts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Cat Fact

| Action | Method | Description |
| --- | --- | --- |
| [Get cat facts](actions/get-cat-facts.md) | GET |  |

