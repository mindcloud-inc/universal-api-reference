# icanhazdadjoke: Universal API

Fetch random dad jokes, retrieve jokes by ID, and search the icanhazdadjoke catalog.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/icanhazdadjoke/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://icanhazdadjoke.com
- **Vendor API docs:** https://icanhazdadjoke.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Dad Joke](actions/fetch-dad-joke.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/icanhazdadjoke/latest/actions/fetch-dad-joke?connectionId=$CONNECTION_ID&jokeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Joke

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Dad Joke](actions/fetch-dad-joke.md) | GET | Retrieves a specific dad joke from icanhazdadjoke. |
| [Fetch Random Dad Joke](actions/fetch-random-dad-joke.md) | GET | Retrieves a random dad joke from icanhazdadjoke. |
| [Search Dad Jokes](actions/search-dad-jokes.md) | GET | Finds dad jokes in icanhazdadjoke by search term. |

### Slack Dad Joke

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Random Slack Dad Joke](actions/fetch-random-slack-dad-joke.md) | GET | Retrieves a random dad joke from icanhazdadjoke formatted for Slack. |

