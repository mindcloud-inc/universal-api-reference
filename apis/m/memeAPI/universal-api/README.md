# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423597736.png" alt="Meme API logo" width="28" height="28"> Meme API: Universal API

Meme API through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/memeAPI/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Memes From Subreddit](actions/fetch-memes-from-subreddit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memeAPI/latest/actions/fetch-memes-from-subreddit?connectionId=$CONNECTION_ID&subreddit=string&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Meme

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Random Meme](actions/fetch-random-meme.md) | GET |  |
| [Fetch Random Meme From Subreddit](actions/fetch-random-meme-from-subreddit.md) | GET |  |

### Meme Batch

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Memes From Subreddit](actions/fetch-memes-from-subreddit.md) | GET |  |
| [Fetch Random Memes](actions/fetch-random-memes.md) | GET |  |

