# RAWG Video Games Database: List Games

Retrieves games from RAWG Video Games Database.

```
GET https://connect.mindcloud.co/v1/universal/rAWGVideoGamesDatabase/latest/actions/list-games
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAWG Video Games Database `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAWGVideoGamesDatabase/latest/actions/list-games?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAWGVideoGamesDatabase/latest/actions/list-games?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Search query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchPrecise` | boolean | no | Disable fuzziness for the search query. |
| `searchExact` | boolean | no | Mark the search query as exact. |
| `ordering` | string | no | Sort games by name, released, added, created, updated, rating, or metacritic. Prefix with - for descending. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RAWG Video Games Database API returns.

## Native endpoint

Through the native RAWG Video Games Database API, this operation is `GET /games` (base URL `https://api.rawg.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-games.md) for the provider-specific parameters and requirements.

