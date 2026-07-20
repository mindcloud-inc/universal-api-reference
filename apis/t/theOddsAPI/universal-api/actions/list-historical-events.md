# The Odds: List Historical Events

Retrieves historical events from The Odds API.

```
GET https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-historical-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Odds `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-historical-events?connectionId=$CONNECTION_ID&date=string&sport=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "sport": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-historical-events?${params}`, {
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
| `date` | string | yes | Historical snapshot timestamp in ISO 8601 format. |
| `sport` | string | yes | The sport key returned by List Sports. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "next_timestamp": "string",
      "previous_timestamp": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `next_timestamp` | string |  |
| `previous_timestamp` | string |  |
| `timestamp` | string |  |

## Native endpoint

Through the native The Odds API, this operation is `GET /v4/historical/sports/:sport/events` (base URL `https://api.the-odds-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-historical-events.md) for the provider-specific parameters and requirements.

