# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423524838.png" alt="Cataas logo" width="28" height="28"> Cataas: Universal API

Retrieve random, tagged, and captioned cat media plus Cataas cat metadata and tags.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cataas/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cataas.com/
- **Vendor API docs:** https://cataas.com/doc.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Cats](actions/count-cats.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cataas/latest/actions/count-cats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Cat

| Action | Method | Description |
| --- | --- | --- |
| [List Cats](actions/list-cats.md) | GET |  |

### Cat Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Cats](actions/count-cats.md) | GET |  |

### Cat Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Cat Media By ID](actions/get-cat-media-by-id.md) | GET |  |
| [Get Cat Media By ID With Text](actions/get-cat-media-by-id-with-text.md) | GET |  |
| [Get Random Cat Media](actions/get-random-cat-media.md) | GET |  |
| [Get Random Cat Media By Tag](actions/get-random-cat-media-by-tag.md) | GET |  |
| [Get Random Cat Media By Tag With Text](actions/get-random-cat-media-by-tag-with-text.md) | GET |  |
| [Get Random Cat Media With Text](actions/get-random-cat-media-with-text.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Cat Tags](actions/list-cat-tags.md) | GET |  |

