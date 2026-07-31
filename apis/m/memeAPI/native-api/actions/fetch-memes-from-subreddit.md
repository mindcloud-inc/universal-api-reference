# Fetch Memes From Subreddit with Meme API

## Endpoint

- **Method:** `GET`
- **Path:** `/gimme/:subreddit/:count`
- **Base URL:** `https://meme-api.com`
- **Official documentation:** [Fetch Memes From Subreddit](https://github.com/D3vd/Meme_Api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subreddit` | path | `string` | yes | Required subreddit name. |
| `count` | path | `number` | yes | Required meme count (1-50). Maximum length: 50. |
