# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423319126.png" alt="Bunnies.io logo" width="28" height="28"> Bunnies.io: Universal API

Read random bunny metadata and media from the public Bunnies.io API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bunniesio/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bunnies.io/
- **Vendor API docs:** https://bunnies.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Bunny](actions/get-random-bunny.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunniesio/latest/actions/get-random-bunny?connectionId=$CONNECTION_ID&media=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Bunny

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Bunny](actions/get-random-bunny.md) | GET |  |
| [Get Random Bunny Media](actions/get-random-bunny-media.md) | GET |  |

