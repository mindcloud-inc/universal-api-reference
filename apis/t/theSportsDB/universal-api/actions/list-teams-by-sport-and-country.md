# TheSportsDB: List Teams By Sport And Country

Retrieves teams in TheSportsDB by sport and country.

```
GET https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-teams-by-sport-and-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TheSportsDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-teams-by-sport-and-country?connectionId=$CONNECTION_ID&c=string&s=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "c": "string",
  "s": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-teams-by-sport-and-country?${params}`, {
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
| `c` | string | yes |  |
| `s` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "teams": [
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
| `teams` | array<object> |  |

## Native endpoint

Through the native TheSportsDB API, this operation is `GET /search_all_teams.php` (base URL `https://www.thesportsdb.com/api/v1/json/123`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams-by-sport-and-country.md) for the provider-specific parameters and requirements.

