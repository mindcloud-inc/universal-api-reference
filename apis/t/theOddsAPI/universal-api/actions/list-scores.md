# The Odds: List Scores

Retrieves scores for sports events from The Odds API.

```
GET https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-scores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Odds `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-scores?connectionId=$CONNECTION_ID&sport=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sport": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-scores?${params}`, {
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
| `dateFormat` | string | no | Optional timestamp format, unix or iso. |
| `daysFrom` | string | no | Optional number of days from now to include in scores. |
| `eventIds` | string | no | Optional comma-separated event ids to filter scores. |
| `sport` | string | yes | The sport key returned by List Sports. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "away_team": "string",
      "commence_time": "string",
      "completed": true,
      "home_team": "string",
      "id": "string",
      "last_update": "string",
      "scores": [
        {}
      ],
      "sport_key": "string",
      "sport_title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `away_team` | string |  |
| `commence_time` | string |  |
| `completed` | boolean |  |
| `home_team` | string |  |
| `id` | string |  |
| `last_update` | string |  |
| `scores` | array<object> |  |
| `sport_key` | string |  |
| `sport_title` | string |  |

## Native endpoint

Through the native The Odds API, this operation is `GET /v4/sports/:sport/scores/` (base URL `https://api.the-odds-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scores.md) for the provider-specific parameters and requirements.

