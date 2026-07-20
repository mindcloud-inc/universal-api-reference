# TheSportsDB: Search Players

Finds players in TheSportsDB by player name.

```
GET https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/search-players
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TheSportsDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/search-players?connectionId=$CONNECTION_ID&p=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "p": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/search-players?${params}`, {
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
| `p` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "player": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `player` | array<object> |  |

## Native endpoint

Through the native TheSportsDB API, this operation is `GET /searchplayers.php` (base URL `https://www.thesportsdb.com/api/v1/json/123`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-players.md) for the provider-specific parameters and requirements.

