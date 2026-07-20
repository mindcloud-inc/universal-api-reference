# TheSportsDB: Get League Table

Retrieves a league table from TheSportsDB by league and season.

```
GET https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/get-league-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TheSportsDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/get-league-table?connectionId=$CONNECTION_ID&l=string&s=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "l": "string",
  "s": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/get-league-table?${params}`, {
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
| `l` | string | yes |  |
| `s` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "table": [
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
| `table` | array<object> |  |

## Native endpoint

Through the native TheSportsDB API, this operation is `GET /lookuptable.php` (base URL `https://www.thesportsdb.com/api/v1/json/123`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-league-table.md) for the provider-specific parameters and requirements.

