# <img src="https://images.mindcloud.co/apps/icons/humor-api_1771598100157.png" alt="Humor API logo" width="28" height="28"> Humor API: Universal API

Search jokes, memes, gifs, puns, and playful text content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/humorAPI/latest
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://humorapi.com
- **Vendor API docs:** https://humorapi.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Joke](actions/get-random-joke.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humorAPI/latest/actions/get-random-joke?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Gif

| Action | Method | Description |
| --- | --- | --- |
| [Search Gifs](actions/search-gifs.md) | GET |  |

### Joke

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Joke](actions/analyze-joke.md) | GET |  |
| [Create Joke](actions/create-joke.md) | POST |  |
| [Downvote Joke](actions/downvote-joke.md) | PUT |  |
| [Get Random Joke](actions/get-random-joke.md) | GET |  |
| [Search Jokes](actions/search-jokes.md) | GET |  |
| [Submit Joke](actions/submit-joke.md) | POST |  |
| [Upvote Joke](actions/upvote-joke.md) | PUT |  |

### Meme

| Action | Method | Description |
| --- | --- | --- |
| [Downvote Meme](actions/downvote-meme.md) | PUT |  |
| [Get Random Meme](actions/get-random-meme.md) | GET |  |
| [Search Memes](actions/search-memes.md) | GET |  |
| [Upvote Meme](actions/upvote-meme.md) | PUT |  |

### Text

| Action | Method | Description |
| --- | --- | --- |
| [Insult](actions/insult.md) | GET |  |
| [Praise](actions/praise.md) | GET |  |

### Word

| Action | Method | Description |
| --- | --- | --- |
| [Generate Nonsense Word](actions/generate-nonsense-word.md) | GET |  |

### Wordrating

| Action | Method | Description |
| --- | --- | --- |
| [Rate Word](actions/rate-word.md) | GET |  |

