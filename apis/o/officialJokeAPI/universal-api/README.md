# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423589180.png" alt="Official Joke API logo" width="28" height="28"> Official Joke API: Universal API

Get random, typed, and identified jokes from the Official Joke API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/officialJokeAPI/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com/15Dkatz/official_joke_api
- **Vendor API docs:** https://github.com/15Dkatz/official_joke_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Joke by ID](actions/get-joke-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officialJokeAPI/latest/actions/get-joke-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Joke

| Action | Method | Description |
| --- | --- | --- |
| [Get Joke by ID](actions/get-joke-by-id.md) | GET |  |
| [Get Random Joke](actions/get-random-joke.md) | GET |  |
| [Get Random Joke by Type](actions/get-random-joke-by-type.md) | GET |  |
| [Get Random Jokes](actions/get-random-jokes.md) | GET |  |
| [Get Ten Jokes by Type](actions/get-ten-jokes-by-type.md) | GET |  |
| [Get Ten Random Jokes](actions/get-ten-random-jokes.md) | GET |  |

### Joke Type

| Action | Method | Description |
| --- | --- | --- |
| [List Joke Types](actions/list-joke-types.md) | GET |  |

