# TheSportsDB: List Event Lineup

Retrieves event lineups from TheSportsDB by event ID.

```
GET https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-event-lineup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TheSportsDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-event-lineup?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-event-lineup?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lineup": [
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
| `lineup` | array<object> |  |

## Native endpoint

Through the native TheSportsDB API, this operation is `GET /lookuplineup.php` (base URL `https://www.thesportsdb.com/api/v1/json/123`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-lineup.md) for the provider-specific parameters and requirements.

