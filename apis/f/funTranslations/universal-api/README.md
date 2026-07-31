# <img src="https://images.mindcloud.co/apps/icons/fun-translations_1785426493942.png" alt="Fun Translations logo" width="28" height="28"> Fun Translations: Universal API

Fun Translations through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/funTranslations/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Translate to Dothraki](actions/translate-dothraki.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/funTranslations/latest/actions/translate-dothraki?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate to Dothraki](actions/translate-dothraki.md) | GET |  |
| [Translate to Klingon](actions/translate-klingon.md) | GET |  |
| [Translate to Minion](actions/translate-minion.md) | GET |  |
| [Translate to Pirate](actions/translate-pirate.md) | GET |  |
| [Translate to Shakespeare](actions/translate-shakespeare.md) | GET |  |
| [Translate to Yoda](actions/translate-yoda.md) | GET |  |

