# TheSportsDB: List Event Highlights By Day

Retrieves event highlights in TheSportsDB for a specific day.

```
GET https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-event-highlights-by-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TheSportsDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-event-highlights-by-day?connectionId=$CONNECTION_ID&d=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "d": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theSportsDB/latest/actions/list-event-highlights-by-day?${params}`, {
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
| `d` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
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
| `events` | array<object> |  |

## Native endpoint

Through the native TheSportsDB API, this operation is `GET /eventshighlights.php` (base URL `https://www.thesportsdb.com/api/v1/json/123`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-highlights-by-day.md) for the provider-specific parameters and requirements.

