# <img src="https://images.mindcloud.co/apps/icons/xkcd_1776789828198.png" alt="Xkcd logo" width="28" height="28"> Xkcd: Universal API

Access xkcd comic metadata from the official public JSON interface, including the latest comic and a specific comic by number.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xkcd/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xkcd.com
- **Vendor API docs:** https://xkcd.com/json.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Atom Feed](actions/get-atom-feed.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xkcd/latest/actions/get-atom-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Comic

| Action | Method | Description |
| --- | --- | --- |
| [Get Comic](actions/get-comic.md) | GET | Retrieves comic metadata from Xkcd by comic number. |
| [Get Latest Comic](actions/get-latest-comic.md) | GET | Retrieves the latest comic metadata from Xkcd. |

### Comic Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Atom Feed](actions/get-atom-feed.md) | GET | Retrieves the Atom comic feed from Xkcd. |
| [Get RSS Feed](actions/get-rss-feed.md) | GET | Retrieves the RSS comic feed from Xkcd. |

