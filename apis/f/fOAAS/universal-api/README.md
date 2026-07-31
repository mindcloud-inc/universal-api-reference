# <img src="https://images.mindcloud.co/apps/icons/f-oaas_1785420632447.png" alt="FOAAS logo" width="28" height="28"> FOAAS: Universal API

Generate FOAAS profanity-laced messages. This integration intentionally exposes offensive content; use it only where appropriate.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fOAAS/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Asshole](actions/asshole.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/asshole?connectionId=$CONNECTION_ID&from=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Asshole](actions/asshole.md) | GET |  |
| [Back Off](actions/back-off.md) | GET |  |
| [Get Version](actions/get-version.md) | GET |  |
| [Random Message](actions/random-message.md) | GET |  |

### Operation

| Action | Method | Description |
| --- | --- | --- |
| [List Operations](actions/list-operations.md) | GET |  |

