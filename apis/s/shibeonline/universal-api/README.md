# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785429404139.png" alt="Shibe.online logo" width="28" height="28"> Shibe.online: Universal API

Get random Shiba Inu, cat, and bird image results from Shibe.online.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shibeonline/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shibe.online/
- **Vendor API docs:** https://shibe.online/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Bird Images](actions/get-random-bird-images.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shibeonline/latest/actions/get-random-bird-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Bird Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Bird Images](actions/get-random-bird-images.md) | GET |  |

### Cat Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Cat Images](actions/get-random-cat-images.md) | GET |  |

### Shibe Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Shibe Images](actions/get-random-shibe-images.md) | GET |  |

